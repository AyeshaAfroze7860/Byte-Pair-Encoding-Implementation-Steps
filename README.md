# Byte Pair Encoding (BPE) and Autoregressive Causal Language Model

## Overview

This project demonstrates the implementation of a **Byte Pair Encoding (BPE) Tokenizer** and a simple **Autoregressive Causal Language Model (ARLM)** using Python.

The BPE tokenizer learns subword tokens by repeatedly merging the most frequent adjacent symbol pairs. These learned tokens are then used by the autoregressive language model to predict the next token or word in a sequence using previously seen tokens.

This project provides a basic understanding of how modern language models prepare text and generate predictions.

---

## Features

### Byte Pair Encoding (BPE)

- Reads text from a corpus
- Preprocesses text
- Splits words into character-level tokens
- Counts word frequencies
- Finds the most frequent adjacent symbol pairs
- Merges symbol pairs
- Learns merge rules
- Builds the final vocabulary
- Encodes and decodes words

### Autoregressive Causal Language Model

- Uses BPE token IDs as input
- Creates input-target pairs
- Learns token embeddings
- Applies positional encoding
- Uses causal masking
- Predicts the next token based only on previous tokens
- Generates text one token at a time

---

## Project Structure

```
Byte-Pair-Encoding-and-Autoregressive-LM/
│── corpus.txt
│── Byte-Pair Encoding (BPE) and Auto regressive Causal Language Model.ipynb
│── README.md
```

---

## Sample Corpus

```text
playing
played
player
playing
playful
replaying
```


## Sample Output

### BPE

```
Initial Vocabulary

p l a y i n g </w>
p l a y e d </w>
p l a y e r </w>
p l a y f u l </w>
r e p l a y i n g </w>

Most Frequent Pair:
('p', 'l')

Vocabulary After Merge:
pl a y i n g </w>

Merge Rules:
('p', 'l')
('pl', 'a')
('pla', 'y')
```

### Autoregressive Language Model

```
Input:
i love

Predicted Next Word:
you

Input:
how are

Predicted Next Word:
you

Input:
good morning

Predicted Next Word:
everyone
```

---

## Applications

- Natural Language Processing (NLP)
- Chatbots
- Text Generation
- Machine Translation
- Search Engines
- Auto-complete Systems
- Large Language Models (LLMs)

---

## Advantages

- Reduces vocabulary size using subword tokenization
- Handles unknown words effectively
- Improves text representation
- Generates context-aware predictions
- Demonstrates the working of modern language models

---

## Limitations

- Prediction quality depends on the training corpus.
- Small datasets provide limited predictions.
- This implementation is for educational purposes and is not a full transformer model.


## Learning Outcomes

After completing this project, you will understand:

- Byte Pair Encoding (BPE)
- Subword Tokenization
- Vocabulary Learning
- Merge Rules
- Autoregressive Language Modeling
- Next Token Prediction
- Basic Language Model Pipeline

