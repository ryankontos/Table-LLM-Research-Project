### **Research Logbook**

**Researcher:** Ryan Kontos  

---

#### **Monday, 19th August 2024**  
- **Tasks:**  
  - Started reading "Table Meets LLM: Can Large Language Models Understand Structured Table Data?"  
  - Took notes on the key challenges LLMs face with structured data, particularly tables.  
  - Began researching different serialisation methods used for converting tables into formats that LLMs can better process.  
- **Reflections:**  
  - The paper offers valuable insights into the limitations of current LLMs with structured data, setting a good foundation for the project.

---

#### **Tuesday, 20th August 2024**  
- **Tasks:**  
  - Continued reading the Microsoft paper, focusing on the SUC (Structural Understanding Capabilities) benchmark.  
  - Researched tools and libraries for parsing PDFs, deciding on `pdfplumber`.  
  - Drafted an outline of a document explaining table serialisation techniques.  
- **Reflections:**  
  - The SUC benchmark seems useful for evaluating how well LLMs can handle structured data, particularly tables.

---

#### **Wednesday, 21st August 2024**  
- **Tasks:**  
  - Continued working on the table serialisation document, adding examples for row-wise, column-wise, and cell-wise serialisation.  
  - Explored options for fine-tuning LLMs locally, focusing on tools like Hugging Face’s `Transformers` library and `PyTorch`.  
  - Researched how to generate data to create a robust dataset for fine-tuning.  

---

#### **Thursday, 22nd August 2024**  
- **Tasks:**  
  - Created a GitHub repository for the project, setting it up to track all documents, notes, and code.  
  - Improved the table serialisation document, refining explanations and ensuring the examples are clear and easy to understand.  
  - Investigated different testing techniques to evaluate LLM performance after fine-tuning, including using benchmarks like SUC.  
  - Experimented with the OpenAI API to understand how to interact with the model, focusing on table-related queries. 

---

#### **Tuesday, 27th August 2024**  
- **Tasks:**  
  - Resumed work after being sick. Reviewed the table serialisation document and made further improvements, adding clearer definitions and refining the examples.  
  - Revisited the Microsoft paper to ensure all key concepts were understood and applicable.  
  - Explored the structure and content of the intermediary layer that will handle table parsing and conversion to Markdown.  
- **Reflections:**  
  - Caught up on some missed work, the serialisation document is now much more polished.

---

#### **Wednesday, 28th August 2024**  
- **Tasks:**  
  - Finalised the table serialisation document.
  - Documented a rough outline of the intermediary parsing layer's architecture, focusing on how it will integrate with the LLM. 

---

#### **Friday, 30th August 2024**  
- **Tasks:**  
  - Added initial research questions to the repository. These focus on how well LLMs can be adapted to handle tabular data and what methods can improve code generation in this context.  
  - Started reorganising the project folder structure to make the repository cleaner, separating the paper notes, code, and research components.  

---

#### **Saturday, 31st August 2024**  
- **Tasks:**  
  - Continued with repository reorganisation, moving research papers and summaries into their own folders.
  - Removed irrelevant files to declutter the workspace.  
  - Added the first summary for the "Attention is All You Need" paper, focusing on key principles that could be useful in understanding transformer models.  

---

#### **Tuesday, 3rd September 2024**  
- **Tasks:**  
  - Added more summary notes for key papers, compiling the findings into the main research README for easy access.  
  - Began researching potential approaches for evaluating LLM performance on tabular data, considering the use of real-world datasets.  

---

#### **Friday, 5th September 2024**  
- **Tasks:**  
  - Researched additional testing methods and benchmarks for LLMs in structured data contexts.  
  - Wrote a Python program for converting PDF documents with tables into text with the tables as markdown.

---

#### **Saturday, 7th September 2024**  
- **Tasks:**  
  - Cleaned up the repository, added missing folders for better organisation of future papers.  
  - Continued with research on multi-agent LLM approaches, taking notes on how they could be applied to tabular data tasks.  
- **Reflections:**  
  - The idea of multi-agent systems is promising. Breaking down complex queries may improve the overall accuracy of code generation.

---

#### **Tuesday, 10th September 2024**  
- **Tasks:**  
  - Modified the README in the repository. 

---

#### **Sunday, 15th September 2024**  
- **Tasks:**  
  - Performed a cleanup of the repository to remove unnecessary files and streamline the workspace.  
- **Reflections:**  
  - The repository is now much cleaner and better organised.

---

#### **Wednesday, 18th September 2024**  
- **Tasks:**  
  - Summarised the TableGPT and TaBERT papers. These gave me insights into how LLMs can be adapted to handle table-related queries through pre-training and techniques for tabular reasoning.  
- **Reflections:**  
  - Pre-training and tabular-specific adaptations seem to be crucial for accurate table reasoning.

---

#### **Friday, 20th September 2024**  
- **Tasks:**  
  - Summarised the SpreadsheetLLM paper. 

---

#### **Tuesday, 24th September 2024**  
- **Tasks:**  
  - Summarised the TabFact paper, which focuses on verifying facts in tabular data.  
  - Experimented with the OpenAI API.  
- **Reflections:**  
  - Integrating fact verification into the system will improve its robustness, especially when users are querying large, structured datasets. This could be a key feature moving forward.
  - GPT models on their own struggle more than I expected that performing complex queries on a table. Optimisation techniques will be needed.

---

#### **Thursday, 26th September 2024**  
- **Tasks:**  
  - Summarised the "LLM Wizard, Code Wand" paper. It provides strong evidence for the role of code in enhancing LLM reasoning capabilities.  
  - Began exploring how code-generation techniques from this paper could be used to improve the system's ability to query and manipulate tabular data.  

---

#### **Saturday, 28th September 2024**  
- **Tasks:**  
  - Completed a summary of the "LLM based Multi-Agents" paper, which discusses how multiple agents can collaborate on complex tasks. This fits quite well with my plan of having different agents handle different aspects of the query-to-code process in my system.  
  - Began experimenting with basic agent interactions, simulating how they might pass tasks like query generation, code execution, and validation.  
- **Reflections:**  
  - Multi-agent systems will likely play a significant role in optimising how complex user queries are handled. Implementing this approach could greatly improve efficiency and accuracy in code generation.

---

#### **Tuesday, 1st October 2024**  
- **Tasks:**  
  - Summarised the AutoGen paper, which provides a framework for creating multi-agent systems that communicate dynamically.  
  - Ideated initial designs for the agent communication workflow in my project, focusing on how agents will interact to handle query parsing, code generation, and result validation. 
