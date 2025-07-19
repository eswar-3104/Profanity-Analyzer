# Profanity Analyzer

A comprehensive profanity detection and content moderation tool built with Python and Streamlit.

## Features

- **Multi-format Support**: Process TXT, PDF, and DOCX files
- **Dual Processing Modes**:
  - **Censor Mode**: Black out profane words in PDF output
  - **Rephrase Mode**: Replace profane words with appropriate synonyms
- **Smart Detection**: Uses better-profanity library for accurate profanity detection
- **Synonym Replacement**: Leverages NLTK WordNet for context-aware word replacement
- **Professional Output**: Generates watermarked PDF reports
- **Analysis Tracking**: Maintains history of processed documents
- **User-friendly Interface**: Clean Streamlit web interface

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/mrudangameswar/profanity-analyzer.git
   cd profanity-analyzer
   ```

2. **Create and activate virtual environment:**
   ```bash
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Download NLTK data (automatic on first run):**
   ```python
   import nltk
   nltk.download('wordnet')
   ```

## Usage

1. **Run the application:**
   ```bash
   streamlit run app3_chosen.py
   ```

2. **Open your browser** and navigate to `http://localhost:8501`

3. **Upload a document** (TXT, PDF, or DOCX)

4. **Choose processing mode:**
   - **Censor**: Creates PDF with profane words blacked out
   - **Rephrase**: Creates PDF with profane words replaced by synonyms

5. **Click "Analyze"** and download the processed document

## Example

### Input Document:
```
This damn system is bullshit and needs improvement.
What the hell were they thinking?
```

### Censor Mode Output:
```
This [CENSORED] system is [CENSORED] and needs improvement.
What the [CENSORED] were they thinking?
```

### Rephrase Mode Output:
```
This darn system is bull and needs improvement.
What the heck were they thinking?
```

## Dependencies

- streamlit
- python-docx
- PyPDF2
- reportlab
- better_profanity
- pdfplumber
- nltk

## Project Structure

```
profanity-analyzer/
├── app3_chosen.py          # Main application file
├── requirements.txt        # Python dependencies
├── test_document.txt      # Sample test document
├── test_document.docx     # Sample Word document
├── temp/                  # Temporary file storage
└── README.md             # This file
```

## Features in Detail

### Document Processing
- **Text Files (.txt)**: Direct text processing
- **Word Documents (.docx)**: Extracts text from paragraphs
- **PDF Files (.pdf)**: Uses pdfplumber for accurate text extraction

### Profanity Detection
- Uses the `better-profanity` library for robust detection
- Handles various forms of profanity
- Context-aware processing

### Output Generation
- **PDF Creation**: Professional reports using ReportLab
- **Watermarking**: Adds verification watermarks
- **Formatting**: Maintains document structure and readability

### Analysis Tracking
- Session-based history tracking
- Statistics on word counts and profanity percentages
- Timestamp logging

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- **better-profanity** library for profanity detection
- **NLTK** for natural language processing capabilities
- **Streamlit** for the web interface
- **ReportLab** for PDF generation

## Contact

Mrudangam Eswar - mrudangameswar2004@gmail.com

Project Link: [https://github.com/mrudangameswar/profanity-analyzer](https://github.com/mrudangameswar/profanity-analyzer)
