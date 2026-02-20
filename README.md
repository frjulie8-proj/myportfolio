# Julie Portfolio Site

This portfolio uses a DRY project template.
You only add/edit files in `_projects/` for new case studies.

## Quick Start

### 1) Start local preview

```bash
cd "/Users/julie/Desktop/Desktop - Julie’s MacBook Air/BU related/myportfolio"
jekyll serve --baseurl "/myportfolio"
```

Open: `http://127.0.0.1:4000/myportfolio/`

If you changed `_config.yml`, stop and restart the server with `Ctrl + C` and run the command again.

### 2) Add a new project (2 minutes)

1. Copy `_projects/beeson-brewery.md`
2. Rename it (example: `_projects/nyc-real-estate.md`)
3. Edit fields in the file front matter:
   - `title`
   - `subtitle`
   - `order`
   - `one_liner`
   - lists like `snapshot`, `approach`, `insights`
   - `repo_url`
4. Save file

The project will automatically:
- get the same page layout (`_layouts/case-study.html`)
- show on the Projects page (`projects.md`)

### 3) Update existing project content

Just edit the matching file in `_projects/`.
Do not duplicate layout HTML.

### 4) Publish to GitHub

```bash
git add .
git commit -m "Add or update project content"
git push origin main
```

## Files you will edit most

- `_projects/*.md` (project content)
- `_config.yml` (site settings)
- `_includes/nav.html` (shared navigation)

## One-time structure already set

- `_layouts/case-study.html` = reusable case-study template
- `projects` collection in `_config.yml`
- `projects.md` auto-lists all project files