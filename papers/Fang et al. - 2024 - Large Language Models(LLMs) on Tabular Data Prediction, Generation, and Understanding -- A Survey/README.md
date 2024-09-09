## Summary of *"Large Language Models (LLMs) on Tabular Data: Prediction, Generation, and Understanding – A Survey"* by Fang et al. (2024)

### Key Characteristics of Tabular Data

Tabular data, which organises information in rows and columns, differs significantly from the sequential nature of text which large language models are trained to understanding. Common challenges include:
1. **Heterogeneity**: Mixed data types (e.g., numerical, categorical) require special handling.
2. **Sparsity**: Real-world tabular datasets often contain missing or imbalanced data.
3. **Order Invariance**: Unlike text or images, the position of rows and columns is generally not crucial, making standard position-based LLM techniques less effective.
4. **Pre-processing Dependencies**: Proper data pre-processing is critical to avoid information loss or introducing errors like multicollinearity.

### Challenges of Tabular Data Parsing for LLMs

Despite their strengths, LLMs face inherent limitations when working with tabular data:
1. **Structure Complexity**: LLMs are designed to handle sequential data, but tables have multi-dimensional relationships between rows, columns, and headers, which do not align well with the linear format LLMs expect.
   
2. **Positional Encoding**: LLMs use positional encodings to process sequences, but these encodings are insufficient for representing hierarchical structures within tables. This often leads to difficulties in capturing the relationships between different parts of the table, such as headers and corresponding data.

3. **Serialisation Issues**: Converting tabular data into a text format (serialisation) for LLM processing introduces challenges. Many serialisation methods (e.g., simple templates or attribute-value pairs) may lose critical structural information. Moreover, LLMs sometimes struggle with numerical data or categorical values that require deeper understanding.

4. **Hallucinations**: LLMs hallucinate, meaning they can add unrelated or incorrect data when parsing tables, especially when the table's structure is complex or contains sparse data.

### Advances in Tabular Data Parsing

To mitigate these challenges, researchers have explored several advanced techniques:
- **Text-Based Serialisation**: Converting tables into human-readable text or structured formats (like Markdown or LaTeX) improves LLM processing. Markdown format is particularly popular, though LaTeX serialisation has shown promise for handling complex tables more effectively.
  
- **Embedding-Based Approaches**: Fine-tuning models like BERT to better capture the semantic relationships between tabular data elements.

- **Prompt Engineering**: Introducing context-specific instructions or in-context learning examples within prompts has improved LLM performance for table understanding and reasoning tasks.

### Paper Conclusion

LLMs show great potential for handling tasks involving tabular data, but their performance in parsing and understanding structured tables still has limitations. Improved serialisation techniques and better handling of hierarchical relationships between table elements are needed to address these challenges. As LLMs continue to evolve, their application to more structured data types, including mixed text and table documents, will become more feasible, but will require more sophisticated methods to achieve reliable results.