# 🎫 Customer Support Ticket Classifier

A smart and interactive **NLP-based system** to automatically classify customer support tickets into predefined categories using **Machine Learning**. Built using Python, this project helps streamline customer service workflows by reducing manual effort in ticket sorting.

---
## 📚 Project Description

This project leverages **Natural Language Processing (NLP)** and **Machine Learning** to build a classifier that:

- Understands customer queries written in natural language.
- Predicts the appropriate **support category** (e.g., Billing, Technical, Account Issues).
- Provides an **interactive CLI tool** to simulate live ticket entry.
- Logs each ticket entry along with its predicted category.

This helps automate the triaging of tickets in customer support systems, enhancing response time and support efficiency.

---

## ✨ Features

✅ Clean and preprocess raw text  
✅ Remove stopwords and punctuation  
✅ Tokenize and normalize input text  
✅ Convert text to vectors using TF-IDF  
✅ Train a Naive Bayes classifier  
✅ Predict categories for new incoming tickets  
✅ Maintain and display a ticket log  
✅ Fully interactive command-line ticket simulator

---

## 📂 Dataset Format

The input dataset should be a CSV file (`tickets_200.csv`) with at least the following columns:

| Column Name | Description                        |
|-------------|------------------------------------|
| `text`      | The customer's ticket text/message |
| `category`  | The actual label/class of the ticket (e.g., Billing, Tech) |

**Example:**

| text                                      | category       |
|-------------------------------------------|----------------|
| I can't access my account                 | Account Issues |
| How do I update my payment method?        | Billing        |
| App crashes when I open the settings page | Technical      |

---

## 🧠 How It Works

1. **Load CSV file** containing historical support tickets.
2. **Preprocess** the text: lowercase, remove punctuation and stopwords, tokenize.
3. **Transform** the text using `TfidfVectorizer`.
4. **Train** a `MultinomialNB` classifier using the processed vectors.
5. **Predict** new ticket categories using the trained model.
6. **Log** each new input and its prediction in real-time.
