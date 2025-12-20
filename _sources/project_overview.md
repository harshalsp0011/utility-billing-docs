# Project Overview

## Problem Statement

Utility bill auditing is time-consuming and error-prone when done manually. Companies need to validate thousands of bills against complex tariff structures.

**Challenges:**
- Complex tariff documents (500+ pages)
- Manual review takes 2-4 hours per bill
- Human error in calculations
- Difficult to scale

## Our Solution

AI-powered system that automates utility bill auditing through a **3-step tariff analysis pipeline**:
- PDF text extraction with page-by-page processing
- Tariff grouping by Service Classification (SC)
- LLM-based logic extraction using OpenAI GPT-4o-mini
- Automated workflows with Apache Airflow
- Interactive web dashboard

## System Architecture

The system uses a **pipeline-based architecture** with the following components:

### Tariff Analysis Pipeline (3 Steps)

**Step 1: PDF Text Extraction** (`pagewise_text_extractor.py`)
- Extracts text from each PDF page
- Stores raw extracted text in S3 (`raw_extracted_tarif.json`)

**Step 2: Tariff Grouping** (`group_extracted_raw_text.py`)
- Groups tariffs by Service Classification (SC1, SC2, SC3, etc.)
- Organizes rate structures by service class
- Outputs grouped tariffs to S3 (`grouped_tariffs.json`)

**Step 3: LLM Logic Extraction** (`extract_logic_llm_call.py`)
- Uses OpenAI GPT-4o-mini to understand billing logic
- Extracts structured tariff rules and formulas
- Produces final logic output to S3 (`final_logic_output.json`)

### Additional Components

**Document Processor** (`utility_bill_doc_processor.py`)
- Processes utility bill PDFs
- Extracts billing data, account info, consumption

**Audit Calculation Engine** (`calculation_engine.py`, `calc_engine_updated.py`)
- Recalculates charges based on extracted tariff logic
- Compares calculated vs actual charges

**Bill Validation Agent** (`anomaly_detector_llm_call.py`)
- Validates extracted bill data before reporting
- Flags anomalies and missing fields

**Report Generation Agent** (`report_generator.py`)
- Generates structured audit reports from validated bill data
- Summarizes discrepancies, financial impact and audit outcomes

**Supporting Modules**
- `rule_db_loader.py` - Loads tariff rules into database
- `prompts_to_extract_logic.py` - LLM prompt engineering for tariff extraction

## Tech Stack

- **Python 3.10+**: Core language
- **OpenAI GPT-4o-mini**: LLM for tariff logic extraction and analysis
- **PostgreSQL**: Primary database (AWS RDS cluster)
- **Apache Airflow 3.1.0**: Workflow orchestration with REST API v2
- **Streamlit**: Interactive web dashboard "The Agentic Auditor"
- **Docker & Docker Compose**: Containerization
- **AWS S3**: File storage for PDFs and JSON outputs
- **pdfplumber**: PDF text extraction
- **camelot**: Table extraction from PDFs

## Team

**Team Name**: EagleEye

**Members**:
- Harshal Patil
- Avipsa Bhujabal
- Aarushi Jugran

**Course**: CDA 500 Project, University at Buffalo
**Duration**: Fall 2025

## Project Goals

- 95%+ accuracy in bill validation
- Process bills in under 2 minutes
- Reduce manual effort by 90%
- Scalable to 1000+ bills per day
