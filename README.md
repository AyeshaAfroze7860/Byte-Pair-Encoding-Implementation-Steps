# Byte Pair Encoding 

## Overview

This project implements the **Byte Pair Encoding (BPE)** algorithm from scratch using Python. BPE is a subword tokenization technique widely used in Natural Language Processing (NLP) to build an efficient vocabulary by repeatedly merging the most frequent adjacent symbol pairs.

The implementation demonstrates the complete BPE workflow, including reading a text corpus, preprocessing text, counting word and pair frequencies, merging the most frequent symbol pairs, and updating the vocabulary after each merge.


## Features

- Read text from a corpus file
- Convert text to lowercase
- Split words into character-level tokens
- Add end-of-word (`</w>`) symbol
- Count word frequencies
- Find adjacent symbol pairs
- Count pair frequencies
- Merge the most frequent pair
- Update vocabulary after each merge
- Display vocabulary after every iteration


## Project Structure

```
BPE-Tokenizer/
│── corpus.txt
│── bpe.py
│── README.md
```


## Corpus

Example `corpus.txt`

```text
playing
played
player
playing
playful
replaying
```

## Algorithm Steps

1. Read the text corpus.
2. Convert words to lowercase.
3. Split each word into characters.
4. Append the end-of-word symbol (`</w>`).
5. Count word frequencies.
6. Find all adjacent symbol pairs.
7. Count pair frequencies.
8. Select the most frequent pair.
9. Merge the selected pair.
10. Repeat until the specified number of merges is completed.



## Sample Output

```
Initial Vocabulary

p l a y i n g </w> : 2
p l a y e d </w> : 1
p l a y e r </w> : 1
p l a y f u l </w> : 1
r e p l a y i n g </w> : 1

==============================
Merge 1

Most Frequent Pair:
('p', 'l')

Vocabulary After Merge

pl a y i n g </w>
pl a y e d </w>
pl a y e r </w>
pl a y f u l </w>
r e pl a y i n g </w>
```


## Applications

- Natural Language Processing (NLP)
- Large Language Models (LLMs)
- Machine Translation
- Text Classification
- Chatbots
- Text Generation
- Search Engines



## Advantages

- Reduces vocabulary size
- Handles unknown words effectively
- Learns meaningful subword units
- Improves tokenization efficiency
- Used in modern transformer models



## Limitations

- Requires training on a representative corpus
- Multiple merge operations increase processing time
- Learned subwords may not always match linguistic boundaries


## Learning Outcome

Through this project, the Byte Pair Encoding algorithm is implemented from scratch, demonstrating how subword vocabularies are built by iteratively merging the most frequent adjacent character pairs. This provides a practical understanding of one of the foundational tokenization techniques used in modern NLP systems.

