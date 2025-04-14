# 📄 QuantumAI CLI – YAML Task Guide

This guide explains how to define your own analysis tasks using YAML files. These files are required for **local ML analysis**.

---

## ✅ Basic Structure

```yaml
task_name: potential_client
description: Predict if a company is a potential client
type: classification

input_column: content
output_column: label

model: LogisticRegression
vectorizer: tfidf

data_file: data/client_training.csv

output_format:
  - field: url
    from: page.url
  - field: prediction
    from: prediction
  - field: confidence
    from: probability

report_template: |
  ### {url}
  - **Prediction**: {prediction}
  - **Confidence**: {confidence:.2f}%
```

---

## 🧠 Fields Explained

| Field              | Description |
|--------------------|-------------|
| `task_name`        | Unique task ID |
| `description`      | Optional note |
| `type`             | `classification` or `regression` |
| `input_column`     | Column in CSV with text to analyze |
| `output_column`    | Column in CSV with target labels |
| `model`            | ML model (e.g. `LogisticRegression`, `RandomForest`) |
| `vectorizer`       | Feature extraction method (`tfidf`, `count`) |
| `data_file`        | Path to CSV with training data |

---

## 🖨 Output & Formatting

### `output_format`
Defines how to extract fields from results and assign names for reporting.

### `report_template`
A Markdown/HTML/TXT template using `{}` placeholders from `output_format`.

---

## 💡 Tips

- Use consistent column names in CSV and YAML
- All fields in `report_template` must exist in `output_format`
- You can extract from:
  - `page.url`
  - `page.content`
  - `prediction`, `probability`, `keywords`

---

## 🧪 Example Task Use

```bash
quant analyze --url https://example.com --task tasks/social_links.yaml
```

---

Need help? Ask or share your task in the community folder or on GitHub Issues.