# Profanity Analyzer

A web-based content moderation tool built with Python and Streamlit. Automatically detects and processes profane content in documents, featuring intelligent text replacement using NLP techniques and supporting multiple file formats with professional PDF output generation.

## Features
- Detects and censors profane words in uploaded documents
- Rephrases profane content using NLTK WordNet synonyms
- Supports TXT, PDF, and DOCX file formats
- Generates clean, watermarked PDF reports using ReportLab
- Simple, interactive Streamlit web interface
- Logs past analysis for review

## Technologies Used
- Python
- Streamlit
- NLTK
- better-profanity
- ReportLab
- PyPDF2
- pdfplumber
- python-docx

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/eswar-3104/profanity-analyzer.git
   cd profanity-analyzer
   ```
2. Create and activate a virtual environment (recommended):
   ```sh
   python -m venv venv
   venv\Scripts\activate
   ```
3. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```

## Usage
1. Start the Streamlit app:
   ```sh
   streamlit run app.py
   ```
2. Upload a document (TXT, PDF, DOCX)
3. Choose either "Censor" or "Rephrase" mode
4. Download the processed document


