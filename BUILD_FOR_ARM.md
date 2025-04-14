# 🛠 Building QuantumAI CLI for ARM64 (Windows)

This guide explains how to build a working `quantumai-cli.exe` for ARM64 Windows devices (e.g., Surface Pro X, Windows 11 ARM).

---

## 🔧 Requirements

- ✅ Windows ARM64 machine (or Windows ARM VM, e.g., Parallels on Mac M1/M2)
- ✅ Python 3.11+ installed (64-bit ARM version)
- ✅ `pip install pyinstaller`
- ✅ Git + build tools (`pip install .` successfully runs)

---

## 🚀 Build steps

1. **Clone the repository**

```bash
git clone https://github.com/your-user/quantumai-public.git
cd quantumai-public
```

2. **Set up virtual environment**

```bash
python -m venv .venv
.venv\Scripts\activate
pip install .
```

3. **Install PyInstaller**

```bash
pip install pyinstaller
```

4. **Build the ARM64 binary**

```bash
pyinstaller cli.py --name quantumai-cli-arm64 --onefile --console
```

This will generate:

```
dist\quantumai-cli-arm64.exe
```

---

## 💡 Notes

- You must run this build process **on an ARM64 Windows machine**.
- PyInstaller automatically detects the correct architecture.
- You can now replace the placeholder `quant.exe` in the ARM installer zip.

---

For feedback, open an issue:  
👉 [https://github.com/your-user/quantumai-public/issues](https://github.com/your-user/quantumai-public/issues)