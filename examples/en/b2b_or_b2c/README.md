# 🏢 B2B or B2C Classifier

Determine whether a company primarily serves businesses (B2B) or consumers (B2C).

---

## 📊 Classification Labels

- `b2b`
- `b2c`

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
Example text about topic 1,b2b
Example text about topic 2,b2c
```