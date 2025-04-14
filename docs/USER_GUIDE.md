# 🧠 QuantumAI CLI – User Guide

Welcome to **QuantumAI CLI**, a command-line tool that uses AI (OpenAI or local ML) to analyze website content based on custom YAML-defined tasks.

This guide is written for non-technical users and will walk you through the installation, usage, and basic concepts.

---

## 📦 Installation

You can install the application in two ways:

### 🔹 1. Using the Windows Installer (recommended)

1. Download the `quantumai-cli-setup-<version>.exe` from [GitHub Releases](https://github.com/your-user/quantumai-public/releases)
2. Run the installer. It will:
   - Install the app into `Program Files\QuantumAI-CLI`
   - Add it to your system PATH
   - Install Python if missing
3. Open a terminal (PowerShell or CMD) and type:

```bash
quant --help
```

### 🔹 2. Using pip (advanced users)

```bash
pip install quantum-analyzer-cli
```

---

## ⚙️ Basic Usage

```bash
quant analyze --url <website> --task <task.yaml>
```

Example:

```bash
quant analyze --url https://example.com --task tasks/potential_client.yaml
```

---

## 🔁 CLI Commands

### 🔍 Analyze website

```
quant analyze --url <url> [options]
```

| Option         | Description |
|----------------|-------------|
| `--engine`     | `openai` or `local` (default: local) |
| `--task`       | Path to YAML task (for local engine) |
| `--output`     | Output file basename |
| `--result-format` | `txt`, `markdown`, `json`, `html` |
| `--verbose`    | Enable detailed log |

---

### 🧪 Train local model

```bash
quant train --task <task.yaml>
```

This command loads a CSV file and trains a model on demand, as specified in the YAML task file.

---

## 📄 YAML Tasks

YAML task files define:
- What kind of analysis to run
- Which ML model and vectorizer to use
- Which column to train on
- How to format the output

See [`YAML_TASK_GUIDE.md`](./YAML_TASK_GUIDE.md) for a complete reference.

---

## 🐞 Reporting Issues

If something doesn't work, or you'd like to suggest a feature:
👉 [Create an issue on GitHub](https://github.com/your-user/quantumai-public/issues)