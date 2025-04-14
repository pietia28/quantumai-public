# 🏢 Klasyfikacja B2B vs B2C

Rozpoznaje, czy firma kieruje ofertę do firm (B2B), czy klientów indywidualnych (B2C).

---

## 📊 Etykiety klasyfikacji

- `b2b`
- `b2c`

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
Przykładowy tekst o temacie 1,b2b
Przykładowy tekst o temacie 2,b2c
```