# Autocorrect & Autocomplete using GPT-2 and NLTK

This project leverages **GPT-2** and **NLTK** to perform **autocorrection** and **autocomplete** on English sentences, with contextual understanding and visual feedback. It uses a sample from Jane Austen’s *Emma* (Gutenberg Corpus) and offers insights through word clouds and confidence score plots.

---

## 📁 Project Structure

- `autocorrect_autocomplete.ipynb` – Main Colab notebook with code
- `corrected_words_wordcloud.png` – Word cloud image of corrected words
- `gpt2_confidence_plot.png` – Line graph showing model confidence per word
- Dependencies: `nltk`, `transformers`, `torch`, `matplotlib`, `wordcloud`

---

## 🔧 Features

- ✅ Sentence cleaning and tokenization  
- ✅ Vocabulary building using NLTK corpus  
- ✅ **Autocomplete** using GPT-2  
- ✅ **Autocorrect** using GPT-2 context scoring  
- ✅ Visualization of corrected words and confidence scores

---

## 🧪 Sample Input & Output

### 🔹 Autocorrect  
**Original Sentence:** `thnaks`  
**Corrected Sentence:** `thanks`

### 🔹 Autocomplete  
**Input:** `Did you`  
**Prediction:** `ever look at the faces of your friends and you`

📊 The visualizations (word cloud and confidence score plot) are generated based on the above examples.

---

## 📷 Sample Visualizations

### 🟣 GPT-2 Confidence Score Plot
![GPT-2 Confidence]([gpt2_confidence_plot.png](https://github.com/gagandeep1763/Autocorrect-Autocomplete-with-GPT-2-and-NLTK/blob/main/gpt2_confidence_plot.png))

### 🟢 Word Cloud of Corrected Words
![Word Cloud]([corrected_words_wordcloud.png](https://github.com/gagandeep1763/Autocorrect-Autocomplete-with-GPT-2-and-NLTK/blob/main/corrected_words_wordcloud.png))

---

## 💡 How It Works

### 🔸 Autocomplete  
Uses GPT-2 to generate the next few words based on user input. Temperature and sampling settings are used for diversity in predictions.

### 🔸 Autocorrect  
Misspelled words are matched with the closest candidates using `difflib`, then ranked using GPT-2 language model loss score based on the context. The best-scoring candidate is selected.

---

## 🧰 Installation & Setup

In Google Colab or a Python environment:

```bash
pip install nltk matplotlib transformers wordcloud torch --quiet
