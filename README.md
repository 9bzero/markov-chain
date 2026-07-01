# markov-chain

Text generation before transformers. Feed it a corpus, pick an n-gram order, generate text.

A Markov chain predicts the next word based on the previous N words. Order 1 produces nonsense. Order 4 starts to look almost coherent. Order 7+ often just reproduces the original.

## How it works

1. Tokenize the corpus into n-grams
2. Build a lookup table: given the last N tokens, what comes next and how often?
3. Start from a seed, sample the next token from the probability table
4. Repeat

No understanding — just pattern repetition. That contrast with modern LLMs is what makes this educational.

## Features

- Paste any corpus (books, lyrics, code — anything works)
- Built-in corpora: Shakespeare, news headlines, Python docs
- Order slider: 1–7
- Character-level or word-level mode
- Highlights which n-grams were copied directly from the corpus

## Run

```bash
npm install && npm run dev
```
