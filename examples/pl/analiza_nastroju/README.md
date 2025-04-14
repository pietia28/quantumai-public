# 🗣️ Analiza nastroju

Analizuje czy ton treści na stronie jest pozytywny czy negatywny.

---

## 📊 Etykiety klasyfikacji

- `pozytywny`
- `negatywny`

---

## 🛠️ Technologia

- Logistic Regression (scikit-learn)
- TF-IDF wektoryzacja
- Trening modelu bezpośrednio z pliku CSV

---

## 📂 Zawartość

- `tasks/...yaml` – definicja zadania
- `data/...csv` – dane treningowe

---

## ▶️ Przykład użycia

```bash
quant analyze --url https://example.com --task tasks/<twoje_zadanie>.yaml
```

---

## 🧪 Przykładowe dane (CSV)

```csv
content,label
Przykładowy tekst o temacie 1,pozytywny
Przykładowy tekst o temacie 2,negatywny
```