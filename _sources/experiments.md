# Experiments & Methods

This section documents all experiments conducted during the project - both successes and failures.

## Experiment Format

For each experiment, document:
- **What** you tried
- **Why** you tried it
- **Results** (success/failure with metrics)
- **Lessons learned**

---

## LLM Model Selection

**Tried**: GPT-4, GPT-3.5, Claude 3, Llama 3

**Winner**: GPT-4 Turbo
- 95% accuracy vs 78% for GPT-3.5
- Best for complex document understanding
- Worth the extra cost

**Lesson**: Don't compromise on LLM quality for financial calculations

---

## Prompt Engineering

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

**Tried**: PyPDF2, pdfplumber, PyMuPDF, Tabula

**Winner**: PyPDF2 + LLM combination
- LLM handles structure understanding
- PyPDF2 for text extraction
- 98% extraction accuracy

**Lesson**: Combine traditional parsing with AI

---

## Architecture Evolution

**Tried**:
1. Monolithic single agent ❌
2. Two-agent system ⚠️
3. Six specialized agents ✅

**Why Multi-Agent Won**:
- Better modularity
- Easier to debug
- Can scale independently
- Each agent is an expert

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

## Add Your Experiments Here

Upload your experiment notebooks to `uploads/experiments/` and document them using this format:

```markdown
## Experiment Title

**Date**: YYYY-MM-DD
**Status**: ✅ Success / ❌ Failed / ⚠️ Partial

**Objective**: What you wanted to achieve

**Approach**: How you did it

**Results**: 
- Metric 1: value
- Metric 2: value

**Outcome**: Success or failure and why

**Lessons Learned**:
- Key insight 1
- Key insight 2
```

## Key Lessons

1. **Start simple** - Don't over-engineer early
2. **Test with real data** - Synthetic data misses edge cases  
3. **LLM quality matters** - Worth paying for GPT-4
4. **Document failures** - They're as valuable as successes
5. **Iterate quickly** - Fail fast, learn fast
