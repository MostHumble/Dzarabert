
# Model Pruning with Dziribert

This repository contains code that demonstrates the process of model pruning using the Dziribert language model as an example. Model pruning is a technique used to reduce the size of deep learning models by removing unnecessary components without significantly sacrificing performance. In this case, we'll be working with Dziribert, a model specifically designed for the Arabizi spcification, which we will prune into working only with the subset of "arabic tokens" (including all kinds of special tokens)

## What's in This Repository?

- **PruneDziribert.ipynb**: This Jupyter Notebook file showcases the entire process of pruning the Dziribert model, including loading the tokenizer, identifying unwanted tokens, saving a modified tokenizer, and modifying the model's embeddings.

## What's Happening in the Code?

1. **Loading and Saving Tokenizers**: The code starts by installing the Transformers library and loading the tokenizer for the Dziribert model. The original tokenizer is saved locally for later modifications.

2. **Identifying Unwanted Tokens**: Unwanted tokens, such as non-alphabetic characters and specific tokens, are identified and marked for removal. The goal is to reduce the vocabulary while preserving meaningful tokens.

3. **Modifying Tokenizer and Vocabulary**: The code creates a modified tokenizer by removing unwanted tokens from the vocabulary. The modified tokenizer is then saved in the new_tokenizer folder.

4. **Modifying Model Embeddings**: The embeddings (word representations) in the Dziribert model are pruned to match the modified vocabulary. This reduces the memory footprint of the model.

5. **Saving Pruned Model**: The final pruned model is saved in the modified_model folder, ready to be used in applications with reduced computational and memory requirements.
