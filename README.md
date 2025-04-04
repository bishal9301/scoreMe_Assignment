# Detecting and Extracting tables from PDFs 
A Node.js tool to extract text from PDF files and export transaction data to an Excel spreadsheet.

## Features
* Extracts text content from PDF files
* Parses transaction data using regular expressions
* Exports parsed data to an Excel file (XLSX format)
* Handles multi-page PDF documents
* Logs extracted data to console

  # Technologies Used
  * Node.js – Core runtime
  * pdf-parse – PDF text extraction
  * exceljs – Excel file generation
  * JavaScript – Custom logic for table boundary detection and formatting

# Installation
Make sure you have Node.js (v14 or higher) installed.
'''git clone <your-repo-url>
cd <project-directory>
npm install'''

# Install dependencies using npm:
 npm install
# Dependencies
* pdfjs-dist ^2.16.105 - PDF parsing library
* exceljs ^4.4.0 - Excel file generation

# Usage
* Place your PDF file in the project directory (default filename: file.pdf)

# Run the script:
 npm start
node index.js

The script will:

* Parse the PDF file
* Extract transaction data matching the pattern: Date Description Amount Balance Type
* Create an Excel file named parsed_transactions.xlsx with the extracted data
* Log the extracted entries to the console

# Configuration
* You can modify the following constants in index.js:
* PDF_FILE_PATH: Path to the input PDF file
* EXCEL_FILE_PATH: Path for the output Excel file
* regex: Regular expression pattern for matching transactions

# Output Format
The Excel file will contain the following columns:

|Date| Description | Amount | Balance after transaction | Type |
|-|-|-|-|-|
|01-APR-2022 | B/F 30 | 30 | 63 | 234.64DRr.
|04-Apr-2022 |  BY 06971000010040 | 25,000 | 30 | 234.66Dr


# Notes
* The script is currently configured to parse bank statement PDFs with a specific format
* You may need to adjust the regular expression pattern for different PDF formats
* The script handles Indian number formatting (e.g., 30,63,234.66)
