# QuantumAI CLI

QuantumAI CLI is a command-line tool that uses AI to analyze website content based on custom tasks.
It supports both OpenAI API and local machine learning models (trained just-in-time using YAML task definitions and training data).

> Current version: **0.0.1-alpha**

---

## ✨ Features

- Website crawler with HTML content extraction
- AI-based analysis using OpenAI or local ML (sklearn, spaCy, transformers)
- YAML task definitions to control:
  - input/output
  - model choice
  - vectorizer
  - report format and structure
- Output: Markdown, HTML, JSON, or TXT

---

## 🛠 Installation (Windows)

Download the latest installer from [Releases](https://github.com/yourname/quantumai-public/releases) and run:

```bash
quant analyze --url https://example.com --task tasks/your_task.yaml
```

---

## 🧪 Examples

```bash
quant train --task tasks/sentiment.yaml
quant analyze --url https://nice.pl --task tasks/potential_client.yaml --result-format markdown
```

---

## 🌍 Community Contributions

You're welcome to contribute:

- YAML tasks → [`/community`](./community/)
- Example CSV or annotated datasets → [`/examples`](./examples/)

Other parts of the codebase are read-only.

---

## 📄 License

See [LICENSE.txt](./LICENSE.txt) – this is a free but **non-modifiable** and **closed-source** project.

---

## 🚧 Disclaimer

This is an early-stage alpha version. The application may behave unexpectedly or produce inconsistent results.