# Autocorrect & Autocomplete using GPT-2 and NLTK

This project implements autocorrection and autocomplete functionality using the GPT-2 language model along with NLTK. It processes English sentences, predicts contextually accurate completions, and corrects spelling errors with confidence visualization. The dataset used is Jane Austen’s *Emma* from the NLTK Gutenberg Corpus.

---

## Project Structure

- `autocorrect_autocomplete.ipynb` – Main Colab notebook
- `corrected_words_wordcloud.png` – Word cloud of corrected words
- `gpt2_confidence_plot.png` – Line graph showing model confidence
- Requirements: `nltk`, `transformers`, `torch`, `matplotlib`, `wordcloud`

---

## Features

- Sentence cleaning and tokenization  
- Vocabulary generation using NLTK corpus  
- Autocomplete using GPT-2  
- Autocorrect using GPT-2 scoring mechanism  
- Word cloud and confidence score visualization

---

## Sample Input and Output

**Autocorrect**  
- Input: `thnaks`  
- Output: `thanks`  

**Autocomplete**  
- Input: `Did you`  
- Output: `ever look at the faces of your friends and you`

Visuals are based on these inputs.

---

## Visualizations

### GPT-2 Confidence Score Plot  
Displays GPT-2 model confidence per word (lower loss means higher confidence):  
![Confidence Plot](https://github.com/gagandeep1763/Autocorrect-Autocomplete-with-GPT-2-and-NLTK/blob/main/gpt2_confidence_plot.png)

### Word Cloud of Corrected Words  
Shows frequently corrected words using NLTK + GPT-2 logic:  
![Word Cloud](https://github.com/gagandeep1763/Autocorrect-Autocomplete-with-GPT-2-and-NLTK/blob/main/corrected_words_wordcloud.png)

---

## How It Works

### Autocomplete  
GPT-2 generates a sequence of probable words based on the given input using token prediction. Sampling methods control the output diversity.

### Autocorrect  
Misspelled words are matched to similar candidates using `difflib`. GPT-2 scores each candidate in context and selects the one with the lowest loss (highest confidence).

---

## Installation

Use the following command in Colab or a Python environment:

```bash
pip install nltk matplotlib transformers wordcloud torch
