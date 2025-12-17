# Utility Billing AI - Documentation

Project docs for the AI-Powered Utility Billing System.

## What's Inside

1. **Project Overview** – Problem, solution, tech stack, team
2. **Experiments** – What we tried, what worked, lessons learned
3. **Deliverables** – Code links, dashboard access
4. **Results** – Performance metrics
5. **Future Work** – Recommendations

## Structure

```
utility-billing-docs/
├── index.md              # Homepage
├── project_overview.md   # Project info
├── experiments.md        # Experiments log
├── deliverables.md       # Links & access
├── results.md            # Metrics
├── future_work.md        # Next steps
└── uploads/              # Files (reports, screenshots, docs)
```

## Build & View Locally

```bash
# From repo root
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt

# Build the book
jupyter-book build .

# Open locally
open _build/html/index.html
```

## Update the Online Book (manual refresh)

1) Re-build the HTML

```bash
# Refreshes the _build/html folder with your latest changes
jupyter-book build .

# If you see stale content, clean first
jb clean .
jupyter-book build .
```

2) Update the website (pushes to gh-pages)

```bash
# Replaces the old website content on the gh-pages branch and pushes
ghp-import -n -p -f _build/html
```

3) Update your source code (recommended)

```bash
git add .
git commit -m "Updated documentation and code"
git push origin main
```

Summary checklist (run inside utility-billing-docs):

```bash
jupyter-book build .
ghp-import -n -p -f _build/html
git push origin main
```

## Publish via GitHub Actions (preferred)

- Workflow: `.github/workflows/pages.yml` builds and deploys on pushes to `main`.
- Site URL: https://harshalsp0011.github.io/utility-billing-docs

## Tips

- Add team/project details in `project_overview.md`.
- Keep experiment notes in `experiments.md`.
- Store assets in `uploads/`.

---

**Built with [Jupyter Book](https://jupyterbook.org/)**
