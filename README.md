
# 📜 Public Policy Insight & Impact Analyzer (PPIIA)

## Project Overview

The **Public Policy Insight & Impact Analyzer (PPIIA)** is an AI-powered platform designed to simplify and analyze government bills and public policy documents.

The system:
- Extracts bill information from PDFs or URLs
- Converts unstructured text into structured JSON
- Uses LLMs for summarization and policy analysis
- Detects risks, opportunities, and stakeholder impact
- Visualizes results in a Streamlit dashboard

---

# System Architecture

```text
Government Bill PDF / URL
            ↓
Text Extraction
            ↓
NLP Preprocessing
            ↓
Structured JSON
            ↓
Langflow Workflow
            ↓
LLM Analysis
            ↓
AI Summary & Insights
            ↓
Streamlit Dashboard
```

---

# Features

## 1. Bill Upload & Extraction
- Upload PDF bills
- Extract content using PDF parsers
- Optional web scraping from Lok Sabha / Rajya Sabha portals

## 2. Structured JSON Generation
The extracted bill text is converted into structured JSON containing:
- Title
- Ministry
- Objective
- Key Provisions
- Stakeholders
- Risks
- Opportunities
- Industry Impact

## 3. AI-Powered Analysis
Using Langflow + LLMs:
- Bill Topic Classification
- Chronology Builder
- Impact Analysis
- Sentiment & Risk Detection
- Citizen-Friendly Summarization

## 4. Dashboard Visualization
Interactive Streamlit dashboard with:
- AI summary panel
- Industry impact analysis
- Timeline visualization
- Downloadable reports

---

# Tech Stack

| Component | Technology |
|---|---|
| Workflow Orchestration | Langflow |
| NLP Processing | NLTK / spaCy |
| LLM Integration | Hugging Face / Gemini |
| Dashboard | Streamlit |
| Visualization | Plotly / NetworkX |
| Backend | Python |
| Data Format | JSON |

---

# Installation

## Install Required Libraries

```bash
pip install streamlit transformers torch pandas numpy plotly pdfplumber PyMuPDF beautifulsoup4 requests networkx scikit-learn sentencepiece langflow google-generativeai
```

---

# Running Langflow

```bash
langflow run
```

Open:

```text
http://127.0.0.1:7860
```

---

# Langflow Workflow

```text
JSON Loader
      ↓
Prompt Template
      ↓
LLM (Gemini / HuggingFace)
      ↓
Impact Analyzer
      ↓
Risk Detector
      ↓
Chat Output
```

---

# Example Prompt Template

```text
You are a public policy analyst.

Analyze this government bill.

Generate:
1. Citizen-friendly summary
2. Risks
3. Opportunities
4. Industry impact
5. Long-term effects
```

---

# Running Streamlit Dashboard

```bash
streamlit run app.py
```

---

# Cloudflare Tunnel Deployment

## Install Cloudflare

```bash
wget -q https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-linux-amd64.deb

dpkg -i cloudflared-linux-amd64.deb
```

## Generate Public URL

```bash
cloudflared tunnel --url http://localhost:8501
```

---

# Project Workflow

```text
PDF Upload
     ↓
Text Extraction
     ↓
JSON Structuring
     ↓
Langflow LLM Pipeline
     ↓
AI Analysis
     ↓
Dashboard Visualization
```

---

# Folder Structure

```text
project/
│
├── app.py
├── bill_data.json
├── requirements.txt
├── README.md
├── outputs/
│   └── summary_report.pdf
└── data/
    └── sample_bill.pdf
```

---

# Sample JSON Structure

```json
{
  "title": "Digital Data Protection Bill",
  "objective": "Protect digital user privacy",
  "stakeholders": [
    "citizens",
    "businesses"
  ],
  "risks": [
    "Compliance burden"
  ]
}
```

---

# Future Enhancements

- Multi-language bill analysis
- RAG-based policy retrieval
- Real-time parliamentary updates
- Interactive policy graphs
- Vector database integration


---

# Conclusion

The PPIIA system demonstrates how AI, NLP, and LLM technologies can improve public policy understanding for citizens, businesses, and governments.

