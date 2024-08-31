### **Notes on: "Table Meets LLM: Can Large Language Models Understand Structured Table Data? A Benchmark and Empirical Study"**

#### **1. Introduction**
- **Goal**: Explore LLMs' ability (GPT-3.5/4) to understand structured data (tables). Introduce SUC benchmark to test this.
- **Problem**: LLMs excel with natural language but struggle with structured data.
- **Contributions**: 
  - **SUC Benchmark**: Evaluates LLMs on table-related tasks.
  - **Self-Augmented Prompting (SAP)**: Technique to enhance LLM's performance by having the model generate additional context before the main task.

#### **2. SUC Benchmark and Methodology**
- **SUC Benchmark**: Tests LLMs on two main abilities:
  - **Partition & Parsing**: E.g., identifying table boundaries, counting rows/columns.
  - **Search & Retrieval**: E.g., finding specific cell values, retrieving data from specific rows/columns.
  
- **Input Design**: 
  - **Serialisation**: Converting tables to a linear text format for LLMs.
  - **Formats**: HTML, JSON, XML, Markdown. HTML works best (likely due to LLMs being trained on web data).
  - **Role Prompting**: Explicitly labeling parts of the table (e.g., headers, rows).
  - **Partition Marks**: Special tags (e.g., "<row>") to indicate structure.

#### **3. Experimentation and Results**
- **Task Performance**:
  - LLMs perform better with HTML, clear format explanations, and role prompting.
  - **Example**: In a table with merged cells, HTML format plus explicit row/column tags helps the LLM detect cell merges more accurately.

- **Self-Augmented Prompting (SAP)**:
  - **Concept**: Before the main task, prompt the LLM to generate useful intermediate information (e.g., key ranges in a column).
  - **Example**: Before asking "What is the maximum value in column X?", first ask the LLM to list all values in column X, helping it to focus on relevant data.
  - **Effectiveness**: Improves accuracy across tasks—LLMs perform better when they "prepare" by generating context.

#### **4. Discussion**
- **LLM Structural Understanding**:
  - LLMs have basic structural understanding but struggle with complex tasks (e.g., detecting exact table size).
  - **Input Design Key**: HTML format + role prompts + partition marks = better performance.

- **Future Work**:
  - Expand SUC to include more varied tables/tasks.
  - Develop advanced prompt engineering techniques to further enhance LLM capabilities.

#### **5. Conclusion**
- **Takeaways**:
  - LLMs can handle structured data somewhat, but with limitations.
  - Proper input design and SAP can significantly improve performance.
- **Impact**: SUC and SAP offer new tools and methods for improving LLMs' understanding of structured data, guiding future research.