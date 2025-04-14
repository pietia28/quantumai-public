# 🤖 Potential Client Detector

Classify whether a company is a potential client based on their website content.

---

## 📊 Classification Labels

- `yes`
- `no`

---

## 🛠️ Technology

- Logistic Regression (scikit-learn)
- TF-IDF vectorizer
- Just-in-time training from your CSV

---

## 📂 Files Included

- `tasks/...yaml` – task definition
- `data/...csv` – training data

---

## ▶️ Usage Example

```bash
quant analyze --url https://example.com --task tasks/<your_task>.yaml
```

---

## 🧪 Sample Input (CSV)

```csv
content,label
Example text about topic 1,yes
Example text about topic 2,no
```