# Quick Start

## Activate venv (required)

```bash
# From main project folder
source venv/bin/activate
```

## Install (1 minute)

```bash
cd utility-billing-docs
pip install -r requirements.txt
```

## Build (1 minute)

```bash
jupyter-book build .
```

## View (1 second)

```bash
open _build/html/index.html
```

## Add Your Content

### Update Project Info

Edit `project_overview.md` - add team names and details

### Document Experiments

Edit `experiments.md` - add what you tried and learned

### Upload Files

```bash
cp my_notebook.ipynb uploads/experiments/
cp report.pdf uploads/reports/
cp screenshot.png uploads/screenshots/
```

### Rebuild

```bash
jupyter-book build .
open _build/html/index.html
```

## Publish to GitHub

```bash
pip install ghp-import
ghp-import -n -p -f _build/html
```

View at: `https://harshalsp0011.github.io/utility-billing-docs`

That's it!
