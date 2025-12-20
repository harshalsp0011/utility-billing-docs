# The Agentic Auditor - Utility Billing AI

## Project Documentation

Welcome to the documentation for **The Agentic Auditor** - an intelligent, multi-agent AI system for automating utility bill auditing, tariff analysis, and overcharge detection.

## Quick Links

- **Code Repository**: [GitHub](https://github.com/harshalsp0011/utility-billing-ai)
- **Live Dashboard**: [Dashboard URL](https://troyandbankprototype.streamlit.app/)
- **Team**: EagleEye | CDA 500 | University at Buffalo

## About the Project

This system uses a **3-step pipeline** and LLM technology to:
- Extracts text from utility bill PDF and stores it in a database
- Extract text from utility tariff PDF documents (page-by-page)
- Group tariffs by Service Classification (SC1, SC2, SC3, etc.)
- Extract billing logic using OpenAI GPT-4o-mini
- Process and validate utility bills automatically
- Calculate charges and detect overcharges
- Generate audit reports

## Key Features

- **3-step tariff analysis pipeline**: Extract → Group → LLM Analysis
- OpenAI GPT-4o-mini for tariff logic extraction
- PDF processing with pdfplumber for text extraction
- Service Classification (SC) based tariff grouping
- Apache Airflow 3.1.0 workflow orchestration with REST API
- Interactive Streamlit dashboard ("The Agentic Auditor")
- AWS S3 storage for processed data and PostgreSQL RDS database
- Automated calculation engine for bill validation

## Navigation

Use the sidebar to explore:
- **Project Overview** - Background, objectives, and team
- **Experiments** - What we tried and what worked
- **UI Showcase** - System interface and project poster
- **Deliverables** - Code, dashboards, and access instructions
- **Results** - Performance metrics and findings
- **Future Work** - Recommendations for next steps
