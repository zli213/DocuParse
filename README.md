# **DocuParse**

## Overview

**DocuParse** is a powerful document processing tool designed to parse and extract text and table information from various types of files including PDF, DOCX, XLSX, and PPTX. This project leverages components from the open-source **[ragflow](https://github.com/infiniflow/ragflow)** project, particularly the **deepdoc** library, which has been adapted and enhanced to meet the specific requirements of this tool.

## Features

- **Multi-format support**: Easily handle and extract content from `.docx`, `.xlsx`, `.pdf`, and `.pptx` files.
- **Text and table extraction**: Efficiently extract and process text and tables from documents.
- **Open-source integration**: Utilizes and extends functionality from the **ragflow** project for advanced document parsing capabilities.

## Installation

### Prerequisites

Ensure you have the following installed:

- Python 3.7 or above
- pip (Python package installer)

### Virtual Environment Setup (Optional)

It is recommended to use a virtual environment to manage your dependencies and avoid conflicts. You can set up a virtual environment as follows:

```bash
# Create a virtual environment
python3 -m venv env

# Activate the virtual environment
# On Windows
env\Scripts\activate
# On Linux/macOS
source env/bin/activate
```

### Required Python Packages

Before using **DocuParse**, you'll need to install the required Python packages. Run the following command to install the dependencies listed in `requirements.txt`:

```bash
pip install -r requirements.txt
```

## Google Gemini API Setup

To integrate **DocuParse** with the [Google Gemini API](https://ai.google.dev/pricing)(I recommend the Gemini1.5 Flash free tier), follow these steps:

### 1. Set Environment Variable

Set your API key as an environment variable. Replace `<YOUR_API_KEY>` with your actual API key.

#### Linux/macOS:

```bash
export API_KEY=<YOUR_API_KEY>
```

#### Windows (Command Prompt):

```cmd
set API_KEY=<YOUR_API_KEY>
```

#### Windows (PowerShell):

```powershell
$env:API_KEY = "<YOUR_API_KEY>"
```

## Usage

To use **DocuParse**, you can execute the `main.py` script, which automatically detects the file type and uses the appropriate parser.

### Command Line Interface

You can run the tool from the command line as follows:

```bash
python main.py <file_path>
```

Replace `<file_path>` with the path to your document.

### Example

```bash
python main.py /path/to/document.pdf
# python main.py '/Users/user/Downloads/Doctors and Health Orgs Feb 2023.pdf'
```

This will output the extracted text content from the specified document.

## Project Structure

- `main.py`: The entry point of the tool, responsible for handling different document formats and initiating the appropriate parser.
- `pdf_parser.py`: Contains the PDF parsing logic.
- `docx_parser.py`: Contains the DOCX parsing logic.
- `excel_parser.py`: Contains the XLSX parsing logic.
- `pptx_parser.py`: Contains the PPTX parsing logic.
- `deepdoc/`: Adapted components from the **ragflow** project for enhanced document parsing.

## Notes

- The **deepdoc** and other document processing components are derived from the **ragflow** open-source project. These components have been modified to fit the needs of **DocuParse**.

## License

This project is licensed under the Apache License 2.0. See the [LICENSE](LICENSE) file for details.

---

With **DocuParse**, you can effortlessly parse and extract valuable information from various document formats, all in a single, streamlined tool.

---
