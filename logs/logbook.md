
### **Research Logbook**

**Researcher:** Ryan Kontos  


#### **Monday, 19th August 2024**
- **Tasks:**
  - Started reading "Table Meets LLM: Can Large Language Models Understand Structured Table Data?"
  - Took notes on the key challenges LLMs face with structured data, particularly tables.
  - Began researching different serialisation methods used for converting tables into formats that LLMs can better process.
- **Reflections:**
  - The paper offers valuable insights into the limitations of current LLMs with structured data, setting a good foundation for the project.

#### **Tuesday, 20th August 2024**
- **Tasks:**
  - Continued reading the Microsoft paper, focusing on the SUC (Structural Understanding Capabilities) benchmark.
  - Researched tools and libraries for parsing PDFs, deciding on `pdfplumber`.
  - Drafted an outline of a document explaining table serialisation techniques.
- **Reflections:**
  - The SUC benchmark seems useful for evaluating how well LLMs can handle structured data, particularly tables.

#### **Wednesday, 21st August 2024**
- **Tasks:**
  - Continued working on the table serialisation document, adding examples for row-wise, column-wise, and cell-wise serialisation.
  - Explored options for fine-tuning LLMs locally, focusing on tools like Hugging Face’s `Transformers` library and `PyTorch`.
  - Researched how to generate synthetic data to create a robust dataset for fine-tuning.
- **Reflections:**
  - The serialisation document is coming together well, and exploring fine-tuning methods has given me a clearer idea of the technical setup needed.

#### **Thursday, 22nd August 2024**
- **Tasks:**
  - Created a GitHub repository for the project, setting it up to track all documents, notes, and code.
  - Improved the table serialisation document, refining explanations and ensuring the examples are clear and easy to understand.
  - Investigated different testing techniques to evaluate LLM performance after fine-tuning, including using benchmarks like SUC.
  - Experimented with the OpenAI API to understand how to interact with the model, focusing on table-related queries.
- **Reflections:**
  - Setting up the GitHub repository helps organise the project, and testing out the API is giving me a better feel for how to structure interactions with the LLM.

#### **Tuesday, 27th August 2024**
- **Tasks:**
  - Resumed work after being sick. Reviewed the table serialisation document and made further improvements, adding clearer definitions and refining the examples.
  - Revisited the Microsoft paper to ensure all key concepts were understood and applicable.
  - Explored the structure and content of the intermediary layer that will handle table parsing and conversion to Markdown.
- **Reflections:**
  - Caught up on some missed work, the serialisation document is now much more polished.

#### **Wednesday, 28th August 2024**
- **Tasks:**
  - Finalised the table serialisation document, ensuring it’s comprehensive and easy to follow.
  - Documented a rough outline of the intermediary parsing layer's architecture, focusing on how it will integrate with the LLM.

