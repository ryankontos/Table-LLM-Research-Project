## Summary: *Attention is All You Need* by Vaswani et al. (2017)

### Background on LLMs

Introduces the Transformer architecture, which revolutionised Large Language Models. Before the Transformer, models relied heavily on recurrent or convolutional neural networks for sequence tasks like language modeling and machine translation. These models faced challenges with: parallelisation and efficiency.

The Transformer bypasses these limitations by relying solely on attention mechanisms. The architecture is built around **self-attention**, allowing the model to process entire sequences simultaneously, instead of sequentially as with recurrent networks. This makes training faster and more scalable, especially for long sequences.

### Key Aspects of the Transformer
- **Self-Attention**: Relates different positions in a sequence to capture dependencies. Each token in the input can "attend" to any other token, which helps in understanding relationships within a document.
- **Multi-Head Attention**: Enhances the self-attention mechanism by projecting the input into multiple subspaces, allowing the model to pay "attention" to different information from the same input sequence.
- **Parallelisation**: The architecture allows for parallel processing of inputs, which makes training faster compared to previous models that rely on sequential processing.

### Limitations with Tabular Data Parsing

While the Transformer architecture is great at processing continuous text, parsing structured tabular data within documents introduces some limitations:

1. **Structured vs. Unstructured Data**: The model is designed for sequential data, and while it can capture semantic relationships between tokens, it struggles with understanding the inherent structure of tables (rows, columns, headers) that don’t follow a linear sequence.
   
2. **Positional Encoding**: The Transformer uses positional encoding to maintain order in sequences, but this approach is less effective for capturing the multidimensional relationships in tables, where data isn’t as sequential.

3. **Lack of Explicit Table Semantics**: The model treats all input as text, meaning it doesn’t natively understand the meaning of rows, columns, or cells in a table. Without special handling, it misses the hierarchical nature of tables (e.g., how a header relates to data underneath).

### Conclusion

The Transformer-based LLMs are powerful for natural language understanding, but their architecture has limitations for parsing tabular data. Addressing these limitations involves exploring new techniques for incorporating table structure and ensuring models can recognise non-sequential patterns in tabular data.