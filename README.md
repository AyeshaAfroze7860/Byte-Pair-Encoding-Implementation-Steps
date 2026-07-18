# Byte Pair Encoding (BPE) Tokenizer

## Overview

This project implements the **Byte Pair Encoding (BPE)** algorithm from scratch using Python. BPE is a subword tokenization technique that builds a vocabulary by repeatedly merging the most frequent adjacent symbol pairs. It is widely used in modern Natural Language Processing (NLP) models to efficiently represent words and handle unknown vocabulary.

The implementation reads a text corpus, learns merge rules, constructs a subword vocabulary, and provides functionality to encode and decode words using the learned vocabulary.

## Features

- Reads text from a corpus file
- Preprocesses text by converting it to lowercase
- Splits words into character-level tokens
- Appends an end-of-word (`</w>`) symbol
- Counts word and symbol pair frequencies
- Learns merge rules using the Byte Pair Encoding algorithm
- Builds a final subword vocabulary
- Encodes new words into subword tokens
- Decodes subword tokens back into the original words
- Displays merge rules, vocabulary, encoded text, decoded text, and vocabulary size


## Project Structure

```
BPE-Tokenizer/
│── corpus.txt
│── bpe.py
│── README.md
```


## Example Corpus

```text
playing
played
player
playing
playful
replaying
```


## Sample Output

```text
Initial Vocabulary

p l a y i n g </w> : 2
p l a y e d </w> : 1
p l a y e r </w> : 1
p l a y f u l </w> : 1
r e p l a y i n g </w> : 1

Most Frequent Pair: ('p', 'l')

Most Frequent Pair: ('pl', 'a')

...

Merge Rules

('p', 'l')
('pl', 'a')
('pla', 'y')

Final Vocabulary

['</w>', 'play', 'player', 'playing', ...]

Vocabulary Size: 18

Original Word : playing
Encoded Word  : ['playing</w>']
Decoded Word  : playing
```


## Applications

- Natural Language Processing (NLP)
- Machine Translation
- Text Classification
- Chatbots
- Search Engines
- Text Generation
- Large Language Models (LLMs)

## Advantages

- Reduces vocabulary size
- Handles unknown words effectively
- Learns meaningful subword units
- Improves tokenization efficiency
- Minimizes out-of-vocabulary (OOV) issues

## Limitations

- Requires a representative training corpus
- Merge operations can be computationally expensive on large datasets
- Learned subwords may not always align with linguistic boundaries


