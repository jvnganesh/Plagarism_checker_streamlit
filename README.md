# Plagiarism Checker with Streamlit

This project is a Streamlit-based application for detecting and highlighting plagiarism between two Word documents. The application compares the contents of two uploaded `.docx` files, identifies plagiarized text, and generates a detailed plagiarism report with highlighted content. The highlighted content and plagiarism report can be downloaded as a new `.docx` file.

## Features

- **Upload Documents**: Users can upload two `.docx` files for comparison.
- **Text Comparison**: The application compares the content of the two documents sentence by sentence.
- **Highlight Plagiarism**: Plagiarized text is highlighted in yellow for similarities > 50% and in red for similarities > 75%.
- **Plagiarism Report**: A detailed report is generated showing the percentage of plagiarized content for each document.
- **Download Report**: The highlighted documents and the plagiarism report can be downloaded as a single `.docx` file.
- **Page-wise Summary**: The application provides a page-wise summary of the plagiarized content on the Streamlit interface.

## How It Works

1. **Document Upload**: Users upload two `.docx` files using the file uploader in the Streamlit interface.
2. **Text Processing**: The contents of both documents are extracted and split into sentences.
3. **Similarity Check**: Each sentence in the first document is compared with each sentence in the second document using `difflib.SequenceMatcher` to calculate similarity scores.
4. **Highlighting**: Sentences in the first document that have a similarity score greater than 50% are highlighted. Yellow for > 50% and red for > 75%.
5. **Report Generation**: A new `.docx` file is created, containing the content of both documents with highlighted plagiarism. The first page of each document includes a plagiarism report showing the percentage of plagiarized content.
6. **Download Option**: Users can download the generated `.docx` file containing the highlighted plagiarism and the report.
7. **Summary Display**: The application displays a page-wise summary of the plagiarized content in the Streamlit interface.

## Usage

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/plagiarism-checker.git
    cd plagiarism-checker
    ```

2. Run the Streamlit app:
    ```bash
    streamlit run app.py
    ```

3. Open the Streamlit app in your browser:
    ```
    http://localhost:8501
    ```

4. Upload two `.docx` files for comparison and check the results.

## Dependencies

- streamlit
- nltk
- python-docx
- difflib


