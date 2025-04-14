# 🧠 QuantumAI CLI – User Guide

Welcome to **QuantumAI CLI**, a command-line tool that uses AI (OpenAI or local ML) to analyze website content based on custom YAML-defined tasks.

This guide is written for non-technical users and walks you through installation, usage, and task configuration.

---

## 📦 Installation

### ✅ Using the Windows Installer (recommended)

1. Download the `quantumai-cli-setup-<version>.exe` from [GitHub Releases](https://github.com/pietia28/quantumai-public/releases)
2. Run the installer. It will:
   - Install the app into `Program Files\QuantumAI-CLI`
   - Add it to your system `PATH`
   - Install Python if missing
3. Open a terminal (PowerShell or CMD) and type:

```bash
quant --help
```

---

## 🚀 CLI Commands & Options

### 🔍 `analyze` – Analyze a website

```bash
quant analyze --url <url> [options]
```

| Argument / Option           | Description                                                             |
| --------------------------- | ----------------------------------------------------------------------- |
| `-u`, `--url`               | ✅ (required) URL of the website to analyze                              |
| `-a`, `--api-key`           | API key for OpenAI (only used with `--engine openai`)                   |
| `-mt`, `--max-tokens`       | Max number of tokens (OpenAI engine only, default: 2000)                |
| `-mp`, `--max-pages`        | Max number of pages to crawl (default: 10)                              |
| `-o`, `--output`            | Output file basename (timestamp and domain are added automatically)     |
| `-v`, `--verbose`           | Enable detailed logging to console                                      |
| `-ac`, `--aggressive-crawl` | Enable aggressive crawling (more HTML tag parsing)                      |
| `-e`, `--engine`            | AI engine to use: `openai` or `local` (default: local)                  |
| `-rf`, `--result-format`    | Format output: `txt`, `json`, `markdown`, or `html` (default: markdown) |
| `-t`, `--task`              | Path to YAML task (required for local engine)                           |

---

### 🧪 `train` – Train a local model manually

```bash
quant train --task <path-to-task.yaml>
```

- Loads a local CSV file and trains a model based on YAML configuration.

---

### 💻 `local` – Shortcut for local analysis

```bash
quant local --url <url> --task <task.yaml> [options]
```

Alias for: `quant analyze --engine local`

Same options apply, except OpenAI-specific ones like `--api-key`, `--max-tokens`.

---

## 📄 YAML Tasks

YAML task files define:

- What kind of analysis to perform
- What model/vectorizer to use (for local ML)
- Which training dataset to use
- How to structure the output report (template)

See [`YAML_TASK_GUIDE.md`](./YAML_TASK_GUIDE.md) and [`YAML_TUTORIAL.md`](./YAML_TUTORIAL.md) for more.

---

## 🐞 Reporting Issues

Found a bug or have a suggestion?
👉 [Create an issue on GitHub](https://github.com/pietia28/quantumai-public/issues)

Help us make QuantumAI CLI even better! 🚀