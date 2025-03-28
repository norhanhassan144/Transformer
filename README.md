# Transformer
Overview

This script demonstrates how to compute self-attention scores for a given sentence using basic mathematical operations. It simulates a Transformer encoder's self-attention mechanism by:

Representing words as numerical vectors (embeddings)

Computing attention scores using the dot product

Applying softmax normalization to obtain final attention weights

Code Explanation

1. Sentence Processing

The sentence used is:

"What are the symptoms of diabetes?"

Each word is assigned a simulated word embedding (3-dimensional vector) stored in a dictionary.

2. Building the Embedding Matrix

The word embeddings are collected into a matrix for efficient computation.

3. Computing Self-Attention Scores

The attention scores are computed using the dot product between word vectors.

These scores represent the relationship between words in the sentence.

4. Softmax Normalization

The softmax function is applied to transform raw scores into a probability distribution.

This ensures that attention weights sum up to 1 for each word.

Output

The program prints the self-attention scores for each word in the sentence:

Self-Attention Scores:
What:      [0.152, 0.150, 0.146, 0.180, 0.150, 0.218]
are:       [0.151, 0.152, 0.148, 0.182, 0.148, 0.216]
the:       [0.149, 0.150, 0.155, 0.180, 0.150, 0.213]
symptoms:  [0.124, 0.126, 0.122, 0.197, 0.122, 0.306]
of:        [0.152, 0.149, 0.149, 0.178, 0.153, 0.217]
diabetes:  [0.098, 0.097, 0.094, 0.199, 0.097, 0.413]

Interpretation

Higher values indicate stronger attention relationships between words.

For example, "symptoms" has a strong relation to "diabetes", as expected.

The self-attention mechanism helps the model understand word importance and context.

Requirements

Python 3

NumPy library
