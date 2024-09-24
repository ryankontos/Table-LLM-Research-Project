**Title**: _TabFact: A Large-scale Dataset for Table-based Fact Verification_  
**Authors**: Wenhu Chen, Hongmin Wang, Jianshu Chen, Yunkai Zhang, et al. (2019)

### Key Insights Relevant to My Thesis:

1. **Introduction of TabFact**:
   - **TabFact** introduces a dataset designed for the verification of natural language statements against semi-structured tables. The dataset includes 118k manually annotated statements linked to 16k Wikipedia tables, where statements are classified as either **entailed** or **refuted** based on the table’s content.

2. **Mixed Reasoning: Linguistic and Symbolic**:
   - The paper highlights the complexity of combining **linguistic reasoning** (understanding paraphrased or inferred statements) and **symbolic reasoning** (executing operations such as counting, summing, and comparing data values from tables).
   - This distinction is highly relevant for my project. A conversational agent needs to understand both types of reasoning to generate accurate code. For instance, a query that requires counting entries in a column involves symbolic reasoning, while interpreting synonyms or inferred information requires linguistic reasoning.

3. **Verification Methods: Table-BERT and LPA**:
   - **Table-BERT** leverages a pre-trained BERT model to linearise the table and combine it with the natural language statement. This model is excellent at linguistic reasoning but struggles with symbolic reasoning since it does not inherently execute operations.
   - **Latent Program Algorithm (LPA)**, on the other hand, transforms statements into programs that execute over the table (using APIs like `count`, `argmax`, `filter`), providing better symbolic reasoning but being more complex to implement.
   - For my thesis, combining elements of both approaches could be a promising strategy. Table-BERT’s natural language understanding could handle query comprehension, while a program-based approach like LPA could handle code generation for tabular operations.

4. **Table Fact Verification Task**:
   - The task is defined as verifying whether a natural language statement is true (entailed) or false (refuted) given a table. For instance, a statement like "There are three Democrats" requires checking if the table contains three rows where the "Party" column equals "Democratic".

5. **Linguistic vs. Symbolic Challenges**:
   - **Linguistic Reasoning**: Involves interpreting paraphrased statements and inferring meanings (e.g., "John was re-elected" requires understanding the term "won").
   - **Symbolic Reasoning**: Involves operations on the table (e.g., counting rows that satisfy certain conditions or finding maximum values).

6. **Dataset Structure**:
   - The dataset is split into **simple** and **complex** channels. Simple statements often reference a single row and involve basic operations, while complex statements require cross-row reasoning, higher-order operations (like counting or finding maximum values), and logical inference.

7. **Program-Based Verification Approach**:
   - LPA parses natural language statements into symbolic programs using functions such as `argmax`, `min`, and `count`, which are executed to verify the statements. The symbolic execution approach ensures interpretability and allows for explicit reasoning steps.
   - This method is applicable to my project, as my system will generate code to process and query tabular data. Implementing a similar API-based system to translate natural language queries into code operations could streamline the process of generating accurate and efficient code although it sounds quite complex.

8. **Error Analysis**:
   - The paper’s analysis shows that **spurious programs** (incorrect programs that happen to return correct results) are a significant challenge for LPA. Similarly, Table-BERT struggles with long dependency chains and understanding table structure when presented in linearised format.
   - These insights are important for my thesis because my system needs to be robust enough to avoid generating erroneous or overly complex code when handling ambiguous or indirect queries, or at least able to recover from errors by reattempting and learning from its mistakes.

### Example Applications in My Thesis:

- **Fact Verification Queries**: When a user asks, “Are there three Democrats in the data?” the agent could use an approach similar to LPA to generate a `filter` function for the "Party" column and then a `count` operation to verify the answer.
- **Combining Linguistic and Symbolic Reasoning**: For queries that involve a combination of linguistic and symbolic reasoning (e.g., “Find the candidate with the highest vote count”), the agent could use a Table-BERT-like model for understanding and then generate code to execute symbolic operations like `argmax`.
