**Title**: _SpreadsheetLLM: Encoding Spreadsheets for Large Language Models_  
**Authors**: Yuzhang Tian, Jianbo Zhao, Haoyu Dong, et al. (2024)

1. **Challenges in Spreadsheet Processing for LLMs**:
   - The complexity and two-dimensional structure of spreadsheets present unique challenges for LLMs, which are typically optimised for sequential, text-based data. Spreadsheets often contain large grids that exceed token limits, as well as cell-specific formats that are difficult to capture.

2. **SHEETCOMPRESSOR**:
   - **SHEETCOMPRESSOR** is an innovative encoding framework designed to compress spreadsheet data effectively for LLMs. It is composed of three main modules:
     - **Structural-anchor-based extraction**: Identifies significant boundaries in the table (headers, relevant rows, and columns) while removing homogeneous rows/columns that contribute minimally to understanding.
     - **Inverted-index translation**: Aims to optimise token usage by indexing non-empty cells and aggregating identical values across cell ranges.
     - **Data-format-aware aggregation**: Groups cells with similar data formats and clusters adjacent numerical cells, improving encoding efficiency.
   - For my project, this encoding approach could serve as an inspiration to pre-process large datasets, ensuring that the conversational agent generates executable code that efficiently interacts with compact, structured data.

3. **Vanilla Spreadsheet Encoding**:
   - The paper proposes a **vanilla encoding** method that serialises spreadsheets into text, capturing essential details like cell addresses, values, and formats. However, this method exceeds token limits when applied to large spreadsheets.
   - This might be useful in my project for smaller datasets.

4. **Compression and Efficiency Gains**:
   - SHEETCOMPRESSOR achieves significant improvements in token efficiency, reducing token consumption by up to 96% and compressing spreadsheets by a factor of 25×. This makes it feasible to process large datasets within the token limits of LLMs.

5. **Chain of Spreadsheet (CoS) for Reasoning**:
   - The **Chain of Spreadsheet (CoS)** approach is introduced to break down spreadsheet reasoning tasks into a structured pipeline: table detection, matching, and reasoning. Chain of thought style.
   - My conversational agent could break down queries about tabular data into sub-tasks: identify the relevant table, extract the necessary rows and columns, and then generate code to process the data.

6. **Fine-Tuning for Spreadsheet QA Tasks**:
   - The paper shows how **fine-tuning** LLMs on spreadsheet-specific tasks improves performance, particularly on spreadsheet QA tasks where the model is required to extract, understand, and reason about table data.

7. **Performance in Table Detection and QA Tasks**:
   - SPREADSHEETLLM outperformed previous models in tasks such as spreadsheet table detection and QA, achieving a 12.3% improvement over the state of the art. It was particularly effective in identifying table boundaries and generating accurate responses to complex spreadsheet queries.

8. **Handling Large, Multi-Table Spreadsheets**:
   - One of the key challenges highlighted is handling large spreadsheets that exceed token limits or contain multiple tables. The SHEETCOMPRESSOR method successfully compresses and segments these large datasets, ensuring that only relevant portions are processed.
   - In my project, this could translate to dynamically splitting large datasets into manageable portions before generating code, allowing the system to focus on the most relevant sections of the data.

9. **Ablation**:
   - The ablation studies show the importance of each component, with significant degradation when any module is removed. This highlights the importance of a comprehensive approach to encoding and compressing spreadsheet data.

### Applications for My Thesis:

- **Efficient Code Generation**: By adopting SHEETCOMPRESSOR’s techniques, my conversational agent could efficiently generate SQL or Python code to process even large datasets, compressing the data into a format manageable by LLMs.
- **Structured Reasoning**: Using the Chain of Spreadsheet method, the system could break down complex queries about tabular data into sequential steps, generating code that accurately reflects the user’s intent and the structure of the dataset.
- **Fine-Tuning for Specific Domains**: Fine-tuning the LLM on specific types of tabular data (e.g., financial, scientific) could improve its ability to handle specialised queries, enhancing the accuracy of the code generated for these datasets.
