# Upload Folder Instructions

## 📁 Folder Structure

This folder is organized to make it easy for you to add your project materials. Simply place your files in the appropriate subfolders, and they'll be automatically accessible from your documentation.

### 📂 `experiments/`
Place all your experimental notebooks, scripts, and code here:

- **`llm/`** - LLM experiments (model selection, prompting, fine-tuning)
  - Example: `model_comparison.ipynb`, `prompt_engineering.py`
  
- **`data_processing/`** - PDF parsing and data extraction experiments
  - Example: `pdf_parsing_tests.ipynb`, `extraction_accuracy.csv`
  
- **`agents/`** - Agent architecture and development experiments
  - Example: `multi_agent_tests.ipynb`, `agent_communication.py`

### 📂 `reports/`
Add analysis reports, metrics, and validation results:

- **`performance/`** - System performance benchmarks
  - Example: `speed_analysis.pdf`, `accuracy_metrics.xlsx`
  
- **`case_studies/`** - Real-world case studies and examples
  - Example: `customer_a_analysis.pdf`, `complex_tariff_case.md`
  
- **`validation/`** - Testing and validation reports
  - Example: `test_results.csv`, `validation_summary.pdf`

### 📂 `deliverables/`
Store final deliverables and documentation:

- **`docs/`** - User guides, API docs, admin manuals
  - Example: `user_guide.pdf`, `api_documentation.html`
  
- **`sample_reports/`** - Example outputs from the system
  - Example: `audit_report_sample.pdf`, `anomaly_report.pdf`
  
- **`videos/`** - Demo videos and tutorials
  - Example: `system_demo.mp4`, `setup_tutorial.mov`
  
- **`kubernetes/`** - K8s deployment manifests
  - Example: `deployment.yaml`, `service.yaml`
  
- **`terraform/`** - Infrastructure as code
  - Example: `main.tf`, `variables.tf`

### 📂 `architecture/`
Add system diagrams and architectural documentation:

- Example: `system_diagram.png`, `data_flow.svg`, `logo.png`
- Recommended tools: Draw.io, Lucidchart, Mermaid

### 📂 `screenshots/`
Dashboard and UI screenshots:

- Example: `dashboard_home.png`, `upload_interface.png`, `results_view.png`

## 🎯 How to Use

### 1. Add Your Files

```bash
# Example: Adding an experiment notebook
cp my_experiment.ipynb uploads/experiments/llm/

# Example: Adding a diagram
cp architecture_diagram.png uploads/architecture/

# Example: Adding a report
cp performance_report.pdf uploads/reports/performance/
```

### 2. Reference in Documentation

In your markdown files, reference uploaded content:

```markdown
# Example: Embedding an image
![System Architecture](../uploads/architecture/architecture_diagram.png)

# Example: Linking to a PDF
[Download Performance Report](../uploads/reports/performance/performance_report.pdf)

# Example: Referencing a notebook
See detailed analysis in [LLM Experiments](../uploads/experiments/llm/my_experiment.ipynb)
```

### 3. Rebuild the Book

```bash
jupyter-book build .
```

## 📝 File Naming Best Practices

- Use descriptive names: `llm_model_comparison.ipynb` not `experiment1.ipynb`
- Use underscores, not spaces: `system_architecture.png` not `system architecture.png`
- Include dates for versioned content: `performance_report_2025_01.pdf`
- Keep names concise but clear

## 📊 Supported File Types

### Images
- PNG (recommended for diagrams)
- JPG/JPEG (recommended for photos)
- SVG (recommended for vector graphics)
- GIF (animations)

### Documents
- PDF (reports, guides)
- Markdown (.md)
- Jupyter Notebooks (.ipynb)
- Excel/CSV (data)

### Videos
- MP4 (recommended)
- MOV
- WebM

### Code
- Python (.py)
- YAML (.yml, .yaml)
- JSON
- Any text-based format

## 💡 Tips

1. **Organize as you go** - Don't wait until the end to upload files
2. **Use subfolders** - Create additional subfolders if needed
3. **Keep it clean** - Remove outdated or duplicate files
4. **Document everything** - Add README files in subfolders if helpful
5. **Check file sizes** - Large files (>100MB) may cause issues

## 🔒 Security Notes

- **Never commit sensitive data** - API keys, passwords, personal information
- **Anonymize data** - Remove customer names, account numbers
- **Check NDAs** - Ensure compliance before uploading client data
- **Review before pushing** - Double-check what you're committing

## ❓ Questions?

If you're unsure where to place a file:
- Check the README.md in the root directory
- Look at existing documentation structure
- Ask the team lead
- Create a new subfolder if needed

---

**Happy documenting! 🚀**
