# 🤖 Machine Learning in QuantumAI CLI – Beginner’s Guide

QuantumAI CLI allows you to analyze websites using **machine learning (ML)** – either through OpenAI's cloud API or local models trained from CSV data.

This guide explains what ML is, how it's used in this app, and what you need to know as a non-technical user.

---

## 📘 What is Machine Learning?

Machine Learning is a field of AI that allows computers to learn from examples, instead of being explicitly programmed. In QuantumAI CLI, ML is used to **classify or score** text from websites based on patterns learned from past data.

---

## 🧠 Two ML Engines

### 1. 🛰 OpenAI-based (cloud)
- Uses GPT models (like ChatGPT)
- Requires an API key from [OpenAI](https://platform.openai.com/)
- You provide a custom prompt (not YAML-based)
- Great for flexible language tasks, entity extraction, summarization

### 2. 💻 Local ML Engine
- Trains models on your own computer
- Uses your CSV and YAML files
- No internet or API key needed
- More private and repeatable

---

## 🧰 What ML frameworks are used?

| Framework      | Used For                           |
|----------------|------------------------------------|
| **scikit-learn** | Classic models: LogisticRegression, RandomForest |
| **spaCy**        | Named Entity Recognition (NER), text classification |
| **Transformers** | Powerful language models (BERT, RoBERTa, DistilBERT) |
| **datasets**     | Loading pre-trained data or models |
| **pandas/numpy** | Data wrangling and vector math    |

All of these libraries are installed automatically with the app.

---

## 📁 Where is ML configured?

In your `task.yaml` file:

```yaml
model: LogisticRegression
vectorizer: tfidf
data_file: data/example.csv
```

You tell the app:
- which ML model to use
- how to convert text into numbers (vectorizer)
- where the training data is

---

## 🔠 Vectorizers

To use text in ML, it must be converted to numbers. This is done using a "vectorizer".

| Vectorizer | Description |
|------------|-------------|
| `tfidf`    | Highlights important words (common in ML) |
| `count`    | Counts word frequency (simpler) |

---

## 📊 Model Types

| Model               | What it does |
|---------------------|--------------|
| LogisticRegression  | Fast binary classifier (yes/no, A/B) |
| RandomForest        | Robust decision tree-based model |
| SpaCyClassifier     | ML model trained on entities and categories |
| TransformerModel    | Deep learning (BERT-like) for text understanding |

---

## 🧪 Training the model

Local ML models are trained **just-in-time** from your CSV file:

```bash
quant train --task tasks/my_task.yaml
```

or run `analyze` and it trains automatically if needed.

---

## 📦 Output

ML predictions are used to generate a report per page:

```text
### https://example.com
- Prediction: yes
- Score: 87.4%
- Keywords: smart, devices, home, systems
```

---

## 🛟 I don’t understand ML – can I still use this?

Yes! You only need:
1. A `task.yaml` file
2. A `data/your_data.csv`
3. Run `quant analyze --url ...`

The program does the rest – it builds, trains, and predicts using your data.

---

## 📚 Resources to Learn More

- [Scikit-learn documentation](https://scikit-learn.org/)
- [SpaCy documentation](https://spacy.io/)
- [Transformers by HuggingFace](https://huggingface.co/transformers/)
- [Free AI/ML Crash Course – Google](https://developers.google.com/machine-learning/crash-course)

---

For questions, open an issue on GitHub or reach out in the community.