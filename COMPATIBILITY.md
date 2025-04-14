# 🖥️ QuantumAI CLI – System Compatibility

This document describes the system requirements and compatibility for running the **QuantumAI CLI Windows installer**.

---

## ✅ Supported Operating Systems

| OS Version                  | Architecture | Notes                      |
|----------------------------|--------------|----------------------------|
| Windows 11                 | x86_64       | ✅ Fully supported         |
| Windows 10 (20H2 or newer) | x86_64       | ✅ Fully supported         |
| Windows 8.1                | x86_64       | ⚠️ Limited (manual Python install may be needed) |
| Windows 7 SP1              | x86_64       | ⚠️ Partial, only with Python ≤3.10 |
| Windows Server 2016+       | x86_64       | ✅ GUI mode required       |

---

## 🧠 Processor Architectures

| Architecture | Status | Notes                                |
|--------------|--------|--------------------------------------|
| x86_64       | ✅ Supported | Standard 64-bit systems           |
| ARM64        | ✅ Supported | Use `quantumai-windows-installer-arm64.zip` with ARM-compatible `.exe` |
| x86 (32-bit) | ❌ Not supported | Only 64-bit systems are supported |

---

## 🐍 Python Dependency

| Condition                     | Status |
|------------------------------|--------|
| Python 3.11.5 bundled        | ✅ Yes |
| Auto-installs if missing     | ✅ Yes |
| Manual install required?     | ❌ No  |

---

## ⚠️ Known Limitations

- 🔐 **Admin rights** may be required for PATH setup or Python installation.
- 🛡️ Some antivirus programs may block the installer – allow or whitelist if needed.
- 🧪 This is an **alpha release** – some behaviors may be unstable or incomplete.

---

For feedback or bug reports, please use GitHub Issues:  
👉 [https://github.com/pietia28/quantumai-public/issues](hhttps://github.com/pietia28/quantumai-public/issues)---

## 🔍 Intel CPUs Support

QuantumAI CLI fully supports computers with **Intel processors** that meet the following requirements:

- 64-bit architecture (x86_64)
- Windows 10 or 11 (64-bit)
- At least 4 GB RAM (8 GB recommended)
- Installer includes Python 3.11.5, no manual installation needed

❌ 32-bit Intel systems and Windows versions are **not supported**.