# Transformer

## Self-Attention Mechanism Demonstration 🤖

### Overview 📝
This Python script demonstrates a basic self-attention mechanism using dot-product attention. It applies self-attention to a simple sentence: 

> "What are the symptoms of diabetes?"

Each word is represented by a simulated word embedding, and the attention scores are computed and normalized using the softmax function.

### How It Works ⚙️
1. **Word Embeddings:** Each word in the sentence is assigned a predefined 3-dimensional vector (simulating word embeddings). 📊
2. **Dot-Product Attention:** A self-attention score matrix is computed by taking the dot product of word vectors. 🔄
3. **Softmax Normalization:** The attention scores are normalized using the softmax function to obtain final attention weights. 🔥
4. **Output:** The script prints the self-attention scores for each word in the sentence. 🖨️

### Code Explanation 💡
- **word_vectors:** A dictionary containing simulated embeddings for each word. 📌
- **values:** A matrix representation of the embeddings. 🔢
- **attention_scores:** Computed by taking the dot product of embeddings and applying the softmax function. 🎯
- **softmax function:** Ensures numerical stability and normalizes scores. 📈
- **Final Output:** The script prints the normalized self-attention scores for each word. 📊

### Sample Output 📋
```
Self-Attention Scores:
What: [0.1524501  0.1509332  0.14647245 0.18069984 0.1509332  0.21851121]
are: [0.15121669 0.15273645 0.1482224  0.18285872 0.1482224  0.21674333]
the: [0.14917602 0.15067527 0.15526401 0.18039105 0.15067527 0.21381838]
symptoms: [0.12477969 0.12603375 0.12230889 0.19766026 0.12230889 0.30690852]
of: [0.15203835 0.14902779 0.14902779 0.17841866 0.15356636 0.21792104]
diabetes: [0.09808175 0.09710582 0.09423591 0.19949743 0.09710582 0.41397325]
```


### Understanding the Output 🔍
Each row in the output represents the attention distribution of a word across all words in the sentence, including itself. The values in each row sum to 1, indicating the relative importance of each word to the given word.

- **Higher values** mean a word is paying more attention to another word.
- **Lower values** mean a word is paying less attention.
- The highest values in a row show which words are the most relevant to the given word.
- The word "diabetes" has the highest self-attention score (0.41397325), meaning it heavily focuses on itself. This is common in attention mechanisms as key terms tend to emphasize themselves.
- "Symptoms" places more attention on "diabetes" (0.30690852), indicating a strong relationship between the two words.
- Other function words (e.g., "What," "are," "the," "of") have more evenly distributed attention scores, meaning they don't strongly focus on any specific word.


### Requirements ✅
- Python 3.x 🐍
- NumPy 🔢
