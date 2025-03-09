# Hadoop Anagram Counter

## 📖 Overview
This repository contains a **Hadoop MapReduce** program to **count anagrams** in a text dataset. The program processes words, normalizes them, and groups anagrams together based on their sorted letter composition.

## 🚀 How It Works

### **Mapper (`mapper.py`)**
- Reads text **from STDIN**.
- Converts all words to **lowercase** to ensure case insensitivity.
- **Removes punctuation** and **filters out stopwords**.
- **Sorts letters** in each word to create a unique key for anagram grouping.
- Outputs **(sorted_word, 1)** pairs to **STDOUT**.

### **Reducer (`reducer.py`)**
- Reads **sorted anagram keys** from **STDIN**.
- Sums up occurrences of each anagram key.
- Outputs the **final count of each unique anagram group** to **STDOUT**.

