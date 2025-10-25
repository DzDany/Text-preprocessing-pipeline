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

## 🧩 Example Workflow

```python
import nltk
from nltk.tokenize import word_tokenize
from nltk.corpus import stopwords
from nltk.stem import WordNetLemmatizer
import string

# 1️⃣ Tokenization
text = "Cats are running faster than the dogs."
tokens = word_tokenize(text)

# 2️⃣ Cleaning
stop_words = set(stopwords.words("english"))
tokens = [t for t in tokens if t.lower() not in stop_words and t not in string.punctuation]

# 3️⃣ Lemmatization
lemmatizer = WordNetLemmatizer()
lemmas = [lemmatizer.lemmatize(t) for t in tokens]

print("Original tokens:", tokens)
print("Lemmatized:", lemmas)
