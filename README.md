# Text-Preprocessing-Pipeline
This repository contains a step-by-step text preprocessing pipeline designed for Natural Language Processing (NLP) tasks,using social media or user-generated text.
The notebook demonstrates how raw, noisy text (including emojis, URLs, special characters, and stopwords) can be systematically cleaned and normalized before being used in machine learning or deep learning models.

This preprocessing approach is suitable for:

Sentiment Analysis

Mental Health Detection

Emotion Classification

Transformer-based NLP models (BERT, RoBERTa, etc.)

**🧾 Dataset Description**
The dataset consists of short text samples reflecting emotional and mental health states, such as:

Sadness

Anxiety

Emotional distress

Neutral / stable mood
**🔄 Preprocessing Steps Explained**
Each preprocessing step is applied sequentially to ensure clean and meaningful text for modeling.

**1️⃣ Remove URLs**

Removes all web links to avoid noise.

re.sub(r'http\S+|www\S+', '', text)

**2️⃣ Remove Emojis & Symbols**

Eliminates emojis and non-textual characters that may not be handled well by traditional NLP models.

re.sub(r'[^\w\s,.!?]', '', text)

**3️⃣ Convert to Lowercase**

Standardizes text by converting all characters to lowercase.

text.lower()
**4️⃣ Remove Special Characters & Numbers**

Keeps only alphabetical characters and spaces.

re.sub(r'[^a-zA-Z\s]', '', text)

**5️⃣ Remove Extra Whitespaces**

Ensures consistent spacing between words.

' '.join(text.split())
**6️⃣ Remove Stopwords**

Removes common English stopwords using NLTK, retaining meaningful content words.

[word for word in text.split() if word not in stop_words]
🧩 Preprocessing Pipeline Diagram (Paste in README)

GitHub supports Mermaid diagrams.
You can paste the following directly into your README.md file.

flowchart TD
    
<img width="1240" height="3735" alt="Text Preprocessing Pipeline-2025-12-18-062228" src="https://github.com/user-attachments/assets/49d541ce-0b88-4a50-954c-d21be34faa50" />


