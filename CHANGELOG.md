# 📦 Changelog – QuantumAI CLI

All notable changes to this project will be documented in this file.

---

## [0.0.2-alpha] – 2025-04-17
### Changed
- CLI command `quant` is now available globally in the system terminal
- Removed "Run after install" option from the installer
- Installer now creates empty folders `tasks/` and `data/` during setup
- Cleaned up bundled `tasks` and `data` directories (now distributed empty)

---

## [0.0.1-alpha] – 2025-04-14
### Added
- First public release of QuantumAI CLI
- Website crawling (basic & aggressive)
- Local ML engine: Scikit-learn, SpaCy, Transformers
- OpenAI engine with prompt-based analysis
- YAML-based task system (fully customizable)
- Just-in-time model training from CSV
- Output formatting to Markdown, TXT, JSON, HTML
- CLI commands: `analyze`, `train`, `local`
- Windows installer with embedded Python
- Starter task: `potential_client.yaml`

### Known Issues
- Some features may be unstable (alpha release)
- ARM architecture is not supported

---