# 📰 Automated Data Extraction, Translation, and Classification Pipeline

## Overview

This Python application automates the process of extracting news titles from the Lalit Mauritius website, translating them from Mauritian Creole to English, performing text analysis, and classifying them into predefined categories using machine learning techniques.

## Purpose

The application serves multiple purposes:
- **Data Extraction**: 🕵️‍♂️ Utilizes `requests` and `BeautifulSoup` libraries to fetch HTML content from [Lalit Mauritius](https://www.lalitmauritius.org/) and parse it to extract news titles identified by `<span>` tags with the class `'title'`.
- **Translation**: 🌐 Leverages Hugging Face's `transformers` library to translate Mauritian Creole news titles into English using a pre-trained model (`prajdabre/morisien_english`).
- **Text Analysis**: 🔍 Employs `nltk` for tokenization, stemming, and stop word identification to process and analyze the text content.
- **Data Structuring**: 📊 Constructs a `pandas` DataFrame to organize and store original Mauritian Creole news titles, translated English versions, and predefined classification labels assigned to each news title based on predefined categories.

## Components Used

The application utilizes the following key components:
- **Libraries**: 
  - `requests` and `BeautifulSoup` for web scraping and HTML parsing 🧩
  - `transformers` for accessing pre-trained models for text translation 🌍
  - `nltk` for text processing tasks such as tokenization, stemming, and stop word identification ✂️
  - `pandas` for data manipulation and DataFrame management 📈
  - `sklearn` for building a text classification pipeline (`TfidfVectorizer` and `MultinomialNB`) to preprocess text data and train a classifier 📚

## Detailed Workflow

The workflow can be summarized as follows:
1. **Web Scraping and HTML Parsing**:
   - 🌐 Fetches HTML content from [Lalit Mauritius](https://www.lalitmauritius.org/) using `requests` and parses it with `BeautifulSoup` to extract news titles.
2. **Translation**:
   - 🔄 Translates Mauritian Creole news titles into English using a translation pipeline from `transformers`.
3. **Text Processing and Analysis**:
   - 📝 Uses `nltk` to tokenize and stem Mauritian Creole words.
   - 📊 Counts word frequencies across all news titles and identifies potential stop words based on frequency thresholds using `Counter`.
4. **Data Handling**:
   - 🗂️ Constructs a `pandas` DataFrame to store original Mauritian Creole news titles, their English translations, and associated classification labels.
5. **Machine Learning**:
   - 🤖 Splits the data into training and testing sets using `train_test_split` from `sklearn`.
   - 🛠️ Constructs a text classification pipeline (`make_pipeline` with `TfidfVectorizer` and `MultinomialNB`) to preprocess text data and train a `Multinomial Naive Bayes` classifier.
   - 📈 Evaluates model performance using `classification_report`.

## Installation

To install the required libraries, use:

```bash
pip install requests beautifulsoup4 transformers nltk pandas scikit-learn
```

## Usage

1. **Extract News Titles**:
   - 📰 The script fetches news titles from the specified URL and parses them using `BeautifulSoup`.

2. **Translate News Titles**:
   - 🌍 Uses the `transformers` pipeline to translate titles from Mauritian Creole to English.

3. **Analyze Text**:
   - 🔍 Tokenizes and stems the text, identifies stop words based on frequency.

4. **Classify Text**:
   - 📚 Preprocesses the text data and trains a text classification model. Evaluates the model performance and prints the classification report.

## Example Output

```plaintext
Original: Propozisyon LALIT dan kad Bidze 2024-25 e dan kad kanpayn elektoral: Kontrol lor Itilizasyon Later ek Lamer
Translated: Lalit’s position in the budget 2024-25 and in the electoral

Original: Genocide Blog 48 – Israel loses war, continues genocide and USA gaslights the world
Translated: And the point about Genocide Blog 48 – Israel loses

...
```

## Conclusion

This Python application showcases a comprehensive pipeline for automated data extraction, translation, linguistic analysis, and supervised classification of textual data from web sources. By integrating robust libraries and tools, it facilitates efficient processing and analysis of multilingual textual data, suitable for various applications requiring automated content handling and classification.
---

Thank you for checking out our project!😉 We believe in creating a better world through technology⚙️, and we hope this project contributes to that goal.👍🏻
