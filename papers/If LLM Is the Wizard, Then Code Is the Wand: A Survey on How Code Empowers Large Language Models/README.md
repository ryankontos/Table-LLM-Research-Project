**Title**: _If LLM Is the Wizard, Then Code Is the Wand: A Survey on How Code Empowers Large Language Models_  
**Authors**: Ke Yang, Jiateng Liu, John Wu, et al. (2024)


1. **Code as a Medium for Complex Reasoning**:
   - The integration of code in LLM training allows these models to perform not just language tasks but also complex **reasoning tasks** by breaking down goals into executable steps. Code provides logical structure and precision, enhancing LLMs’ ability to handle intricate, multi-step processes.
   - In my thesis, this reasoning power is directly applicable to interpreting natural language queries about tabular data. For example, understanding a query like "What are the top 5 sales regions?" involves reasoning over the data, filtering, sorting, and combining tasks that can be mapped to Python code execution.

2. **Unlocking Decision-Making Abilities**:
   - Code-trained LLMs excel in **decision-making** by decomposing tasks, executing plans, and refining outputs based on feedback. They can use chain-of-thought reasoning to iteratively solve complex problems by generating code, running it, and analysing results.
   - This ability is critical for my system, where agents must make decisions about how to interact with tabular data dynamically. For instance, if a query asks for a summary of sales, the agent could generate the necessary query, execute it, and then modify it based on the result (e.g., handling missing data or errors in execution).

3. **Program-of-Thought (PoT) Approach**:
   - The paper discusses the **Program-of-Thought (PoT)** paradigm, which involves converting natural language tasks into code to improve reasoning performance. By translating a problem into a formal, verifiable program (e.g., SQL or Python), PoT ensures correctness and mitigates issues like hallucination or incomplete reasoning.
   - For my project, adopting a PoT approach would allow the system to convert user queries into executable code that can interact with tabular data. The system could ensure correctness by running the generated code and verifying that it meets the user’s intent.

4. **Code Enhances Structured Knowledge Representation**:
   - Code enables LLMs to handle **structured knowledge** effectively, such as understanding data tables, markup (HTML), or graphs. LLMs trained with code can translate natural language into operations over structured data, ensuring that they correctly manipulate data according to its schema or structure.
   - This is particularly useful for my work, where the agent needs to translate user queries into operations over tabular data, such as filtering or summarizing rows. The structured format of code helps bridge the gap between the user’s natural language requests and the structured format of the data.

5. **Multi-Agent Collaboration and Role Assignment**:
   - The paper highlights the effectiveness of **multi-agent collaboration**, where different LLM agents specialise in distinct tasks (e.g., generating code, validating outputs). By collaborating, these agents can solve more complex problems than a single LLM agent could handle.
   - This approach fits well with my thesis, where one agent could focus on parsing user queries, another on generating executable code, and a third on validating the results against the original data. For example, one agent could generate an SQL query to filter data, and another could check if the query returns the expected results.

6. **Feedback from Code Execution for Self-Improvement**:
   - Embedding LLMs within a **code execution environment** allows them to gather feedback from the results of executing generated code. This feedback can be used to refine and improve the model’s output, enabling it to self-correct and optimise performance over time.
   - In my system, feedback loops could be implemented where the agent receives feedback from code execution (e.g., errors, incorrect results) and uses it to adjust its logic. This would improve the agent’s ability to handle edge cases and complex queries in tabular data analysis.

7. **Tool Integration and Function Calls**:
   - The paper emphasises the importance of **integrating tools** and external systems into LLM-based agents. LLMs can generate function calls, interact with APIs, or execute code to perform tasks outside of simple language generation.
   - For my project, integrating tools like Python libraries would allow the agent to generate, execute, and verify code dynamically.

8. **Challenges in Code-Driven LLMs**:
   - Some challenges include **learning the correct function invocation** and handling domain-specific libraries (e.g., scientific tools, financial analysis). LLMs need to understand when and how to call the right functions with the correct parameters.
   - In my system, the agent will need to correctly map natural language requests to the relevant operations on tabular data, ensuring that it calls the right functions (e.g., data aggregation, filtering, visualisation) based on the user’s query.

### Example Applications for My Thesis:

- **Data Querying**: A user asks, “Summarise the sales data by region.” The system could break down this query into tasks, such as selecting relevant columns (e.g., "Region" and "Sales"), grouping by region, and summing the sales values, generating executable code (e.g., SQL or Python) for these steps.
- **Error Handling**: If the generated code fails due to a syntax error or incorrect data type, the system could receive feedback from the execution environment, adjust the code, and try again, learning from the error to refine future queries.