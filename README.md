# 🧠 MCP Data Intelligence Bridge

[![Python 3.12+](https://img.shields.io/badge/python-3.12+-blue.svg)](https://www.python.org/downloads/)
[![MCP Protocol](https://img.shields.io/badge/Protocol-MCP-green.svg)](https://modelcontextprotocol.io)
[![uv](https://img.shields.io/badge/Package_Manager-uv-purple.svg)](https://github.com/astral-sh/uv)
[![Data Science](https://img.shields.io/badge/Data_Stack-Pandas-150458.svg)](https://pandas.pydata.org/)

An enterprise-grade **Model Context Protocol (MCP)** server that bridges Large Language Models (like Claude) with local, unstructured datasets. This infrastructure enables secure, real-time data auditing and document processing without uploading sensitive corporate data to the cloud.

## 🌟 Architecture & Capabilities
This server exposes a suite of secure, local tools to the LLM, transforming it from a standard chatbot into an autonomous data analyst:

- **📊 Structured Data Auditing (CSV):** Leverages `pandas` to perform automated statistical summaries, missing value detection, and schema extraction on local datasets.
- **📄 Unstructured NLP Processing (PDF/DOCX):** Utilizes `PyMuPDF` and `python-docx` to extract, chunk, and analyze text and metadata from local documents for context-aware Q&A.
- **⚙️ Native System Integration:** Bridges the gap between AI analysis and human review by autonomously triggering macOS applications (e.g., launching Numbers or Excel to view a specific dataset).

## 🛠️ Technical Stack
- **Core Language:** Python
- **AI Infrastructure:** Model Context Protocol (FastMCP)
- **Data Engineering:** Pandas, PyMuPDF, Python-docx
- **Environment Management:** `uv` (for sub-second dependency resolution)

## 🚀 The Privacy Advantage (Local-First)
Standard AI workflows require uploading sensitive CSVs or proprietary PDFs to third-party servers. This bridge solves that enterprise bottleneck by allowing the LLM to query the data *where it lives*, ensuring zero data leakage while maintaining real-time analytical capabilities.

## 💻 Example Workflow
**User Prompt:** *"Use the bridge to audit the Q3_Sales.csv file on my Desktop. If you find missing values, open the file in Numbers so I can fix them, and summarize the Project_Guidelines.pdf to see how we handle null data."*

**System Response:** The bridge executes the Pandas audit, identifies 4 null rows, triggers the macOS
