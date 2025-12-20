# Experiments & Methods

This section documents all experiments conducted during the project - both successes and failures.

## Experiment Format

For each experiment, we have documented:
- **What** we have tried
- **Why** we tried it
- **Results** (success/failure with metrics)
- **Lessons learned**

---

## LLM Model Selection

**Tried**: GPT-4, GPT-3.5, Claude 3, Llama 3

**Why we tried it:**
To determine which LLM could most accurately parse and extract structured data from diverse and complex utility billing documents, balancing performance, cost and robustness.

**Winner**: GPT-4 mini
- 95% accuracy vs 78% for GPT-3.5
- Best for complex document understanding
- Worth the extra cost

**Lesson**: Don't compromise on LLM quality for financial calculations

---

## Prompt Engineering

**Why we tried it:**
To systematically optimize the instruction formats and contexts that guide the chosen LLM toward consistent, structured JSON output and near-human accuracy, without needing model retraining.

**Approach**: Tested different prompting strategies

**What Worked**:
- Few-shot learning (2-3 examples)
- Explicit JSON schema
- Low temperature (0.1-0.2)
- Asking for citations/page numbers

**Results**: Improved accuracy from 78% to 95%

**Lesson**: Prompt engineering more effective than fine-tuning

---

## PDF Parsing

**Why we tried it:**
Because raw PDF data varies widely in layout and structure; we needed a reliable text extraction baseline before applying LLM understanding, and wanted to quantify how much traditional parsers contributed versus AI understanding alone.

**Tried**: PyPDF2, pdfplumber, PyMuPDF, Tabula

**Winner**: PyPDF2 + LLM combination
- LLM handles structure understanding
- PyPDF2 for text extraction
- 98% extraction accuracy

**Lesson**: Combine traditional parsing with AI

---

## Architecture Evolution

**Tried**:
1. Monolithic single agent
2. Two-agent system
3. Six specialized agents

**Why we tried it:**
To improve scalability, reduce error coupling, and make the system easier to debug as task complexity increased.

**Results**:
- Single agent: failed under complexity
- Two agents: partial improvement
- Multi-agent: successful, production-ready

**Lesson**:
Specialized, modular agents significantly improve accuracy, maintainability, and scalability in complex AI pipelines.

---

## Failed Experiments

### Fine-Tuning GPT-3.5
**Why it failed**: Only improved from 78% to 86%, still below GPT-4's 95%

**Time wasted**: 4 weeks

**Lesson**: Use better base model instead of fine-tuning weaker one

### Rule-Based Calculation Engine
**Why it failed**: Too rigid for tariff variations

**Lesson**: AI flexibility needed for complex rules

---

## Key Lessons

1. **Start simple** - Don't over-engineer early
2. **Test with real data** - Synthetic data misses edge cases  
3. **LLM quality matters** - Worth paying for GPT-4
4. **Document failures** - They're as valuable as successes
5. **Iterate quickly** - Fail fast, learn fast
