# Utility Billing AI - Documentation

Simple documentation for your AI-Powered Utility Billing System project.

## What's Inside

Just 5 simple pages:

1. **Project Overview** - Problem, solution, tech stack, team
2. **Experiments** - What we tried, what worked, lessons learned
3. **Deliverables** - Code links, dashboard access
4. **Results** - Performance metrics
5. **Future Work** - Recommendations

## Structure

```
utility-billing-docs/
├── index.md              # Homepage
├── project_overview.md   # Project info
├── experiments.md        # Experiments log
├── deliverables.md       # Links & access
├── results.md            # Metrics
├── future_work.md        # Next steps
└── uploads/              # Put your files here
    ├── experiments/      # Notebooks
    ├── reports/          # PDFs
    ├── screenshots/      # Images
    └── docs/             # Guides
```

## Build & View

```bash
# Activate venv first
cd /Users/patil/Library/CloudStorage/OneDrive-UniversityatBuffalo/Desktop/MS/2.Course/4.Third_Fourth\ Semester/CDA\ 500/Troy\ \&\ Banks/Code_Base/utility-billing-ai
source venv/bin/activate

# Go to docs folder
cd utility-billing-docs

# Install (first time only)
pip install -r requirements.txt

# Build
jupyter-book build .

# View locally
open _build/html/index.html
```

## Add Your Content

```bash
# Make sure venv is activated
source ../venv/bin/activate
```

1. Edit the `.md` files with your info
2. Upload files to `uploads/` folder
3. Rebuild: `jupyter-book build .`
4. View: `open _build/html/index.html`

## Publish to GitHub Pages

```bash
# Make sure venv is activated
source ../venv/bin/activate

# Install ghp-import (first time only)
pip install ghp-import

# Build
jupyter-book build .

# Publish
ghp-import -n -p -f _build/html
```

Your site will be at: `https://harshalsp0011.github.io/utility-billing-docs`

## Tips

- **Update URLs**: Replace `YOUR_USERNAME` with your GitHub username
- **Add team names**: Edit `project_overview.md`
- **Document experiments**: Use the template in `experiments.md`
- **Upload files**: Put everything in `uploads/` folder

---

**Built with [Jupyter Book](https://jupyterbook.org/)**
