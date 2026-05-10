# Portfolio Website — Quarto + GitHub Pages

Marketing Analytics portfolio built with Quarto, styled in a professional navy/gold theme.

## File Structure

```
quarto-portfolio/
├── _quarto.yml          # Site config, navbar, Google Analytics, theme
├── index.qmd            # Home page (hero, skills, featured projects)
├── assets/
│   ├── custom.scss      # Global CSS (navy/gold palette, cards, KPIs)
│   ├── reveal-custom.scss  # RevealJS presentation theme
│   ├── photo.jpg        # YOUR PHOTO — add this file
│   ├── resume.pdf       # YOUR RESUME — add this file
│   └── og-image.png     # Open Graph image for social sharing (optional)
├── data/
│   └── RPE-Combined-2019-12-19.sav  # Add your data file here
└── pages/
    ├── about.qmd        # Bio, education, skills
    ├── projects.qmd     # Analytics project case studies
    ├── dashboard.qmd    # KPI dashboard + R charts
    └── presentation.qmd # RevealJS EDA presentation
```

## Quick Start

### 1. Install Quarto
Download from https://quarto.org/docs/get-started/

### 2. Open in RStudio or VS Code
Open the `quarto-portfolio/` folder as your project root.

### 3. Personalize
Search for `Your Name` and replace throughout. Key files to update:
- `_quarto.yml` — your name, LinkedIn/GitHub URLs, Google Analytics ID
- `index.qmd` — name, subtitle, institution, project cards
- `pages/about.qmd` — personal statement, education, achievements
- `pages/projects.qmd` — your actual project write-ups and code
- `assets/custom.scss` — tweak colors if desired

### 4. Add your files
- Drop `photo.jpg` in `assets/` and update the `<img>` tag in `index.qmd`
- Drop `resume.pdf` in `assets/`
- Add your data file to `data/` and set `eval: true` in the code chunks

### 5. Preview locally
```bash
quarto preview
```

### 6. Build the site
```bash
quarto render
# Output goes to /docs (configured in _quarto.yml)
```

### 7. Deploy to GitHub Pages
1. Push the entire repo to GitHub
2. Go to **Settings → Pages**
3. Set Source to `main` branch, folder `/docs`
4. Your site will be live at `https://yourusername.github.io/repo-name`

## Google Analytics
In `_quarto.yml`, replace `GA_MEASUREMENT_ID` with your real measurement ID (format: `G-XXXXXXXXXX`).
Get one free at https://analytics.google.com

## Adding More Projects
Copy a project block in `pages/projects.qmd`, add a new `## Project N` section with a callout-note, prose write-up, code chunks, and results table. Each project gets its own heading anchor for deep linking.
