# Task 1: Build a Robust NLP Preprocessing Engine (Advanced)

---

## 📌 Assignment Overview

In real-world Natural Language Processing (NLP) systems, raw text data is often noisy, inconsistent, and unstructured.
This assignment focuses on building a **production-quality NLP preprocessing engine** capable of handling such complex and messy data effectively.

The goal is to design a **modular and reusable NLP pipeline** and validate it using diverse real-world test cases.

---

## 🎯 Learning Objectives

By completing this assignment, the following skills are developed:

* Design a scalable NLP preprocessing pipeline
* Handle real-world text noise such as emojis, URLs, and irregular patterns
* Apply text normalization techniques
* Perform token-level statistical analysis
* Write clean, maintainable, and robust Python code

---

## 🧠 Problem Statement

You are given messy and unstructured real-world textual data.

Your task is to transform this raw text into **clean, structured, and meaningful tokens** that can be effectively used for machine learning models.


##  Features Implemented

*  Text Cleaning (removal of noise, punctuation, emojis)
*  Lowercasing
*  Removal of numbers
*  Removal of URLs and email patterns
*  Handling repeated characters (e.g., "soooo" → "so")
*  Tokenization
*  Stopword Removal
*  Lemmatization
*  Removal of short words (≤ 2, except "no" and "not")
*  Extra space removal
*  Error Handling (empty input, numbers, emojis, None)

---

## 🔄 NLP Pipeline

Raw Text
->
Cleaning
->
Tokenization
->
Stopword Removal
->
Lemmatization
->
Vectorization
->
Model Ready Data

---

##  Testing

The preprocessing function is tested on multiple real-world examples including:

* Emojis 😍
* Numbers (12345)
* URLs (https://example.com)
* Repeated characters ("soooo")
* Mixed case text
* Slang and noisy inputs

---

## Analysis Performed

* Token count per sentence
* Unique tokens
* Average token length
* Frequency analysis using `collections.Counter`

---

## ⚙️ Technologies Used

* Python 
* NLTK
* Regular Expressions (re)
* Jupyter Notebook

---

##  Conclusion

A robust preprocessing engine is a critical first step in any NLP system. This project demonstrates how raw, noisy text can be transformed into structured and meaningful data suitable for machine learning models.
