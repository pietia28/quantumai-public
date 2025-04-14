# 🌐 Wykrywanie linków do mediów społecznościowych

Sprawdza, czy strona zawiera linki do social mediów (Facebook, Instagram, itp.).

---

## 📊 Etykiety klasyfikacji

- `tak`
- `nie`

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
Przykładowy tekst o temacie 1,tak
Przykładowy tekst o temacie 2,nie
```