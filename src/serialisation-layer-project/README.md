## Introduction
This document outlines the key components and workflow of system that converta a PDF document containing tables into a format that is more appropriate for an LLM.

## Objectives
- **Extract** tables from PDF documents accurately.
- **Serialize** the extracted tables into a linear format (Markdown) that is compatible with LLM input.
- **Ensure compatibility** with the fine-tuned LLM by structuring data in a way that maximizes the model’s understanding and reasoning capabilities.

## Key Components

### 1. PDF Parsing Module
- Use `pdfplumber` for parsing PDFs and identifying tables.
- **Functionality**:
  - Identify table boundaries within the PDF.
  - Extract table content, including headers, rows, columns, and any merged cells.
  - Convert table to serialised text.
  - Convert PDF to text and insert tables as text.
- **Output**: PDF convert to string, with tables replaced with their serialised text. 

### 2. Integration with LLM
- Use the OpenAI API, to send the text data string to an LLM, along with the attached user request.
- **Processing**:
  - The LLM processes the input, interpreting the table data based on the structure provided by the intermediary parsing layer.
  - Retrieve and handle the output from the LLM.
- **Output**: LLM-generated responses based on the processed table data.

## First Steps
- **Implementation**: I plan to begin coding the system, starting with the PDF Parsing Module.
- **Testing**: I will develop a set of test cases using various PDF documents to ensure that the intermediary parsing layer functions as expected across different scenarios.
- **Integration**: Once modules are developed and tested, integrate them into the larger system and perform end-to-end testing with the fine-tuned LLM.