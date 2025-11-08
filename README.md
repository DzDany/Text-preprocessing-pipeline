# 🧠 Text Preprocessing Pipeline (Tokenization, Cleaning, Lemmatization)

This project implements a simple **Natural Language Processing (NLP)** pipeline in Python.  
It processes raw text through three main stages: **tokenization**, **cleaning/filtering**, and **normalization (lemmatization)**.

---

## 📋 Overview

The preprocessing pipeline follows these logical steps:

1. **Tokenization**  
   Splits the raw text into basic components (tokens), such as words and punctuation marks.

2. **Cleaning and Filtering**  
   Iterates through the token list to remove unwanted elements:
   - Punctuation symbols  
   - Stopwords (common words with little semantic value)

3. **Normalization (Lemmatization)**  
   Converts the remaining tokens into their canonical form (lemmas).  


---

## ⚙️ Main Components

| Step | Description | Example Library |
|------|--------------|----------------|
| **Tokenizer** | Splits the text into tokens | `nltk.word_tokenize()` |
| **Stopword Removal** | Filters out common words | `nltk.corpus.stopwords` |
| **Lemmatizer** | Reduces words to their root form | `WordNetLemmatizer()` |

---


# 3️⃣ Lemmatization
lemmatizer = WordNetLemmatizer()
lemmas = [lemmatizer.lemmatize(t) for t in tokens]

print("Original tokens:", tokens)
print("Lemmatized:", lemmas)
