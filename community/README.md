# 🤝 Community Contributions

Welcome to the **QuantumAI Community Zone**!  
Here, you can **share your own analysis tasks and training data** to inspire others and help expand the capabilities of QuantumAI CLI.

---

## 🧠 What You Can Contribute

You are encouraged to submit:

- 🧾 **Custom YAML tasks** that define new analysis goals  
- 📊 **Sample training data** (`.csv`) used to train local ML models  
- 🌍 **Localized tasks** in other languages (e.g., `pl/`, `en/`, `de/`)

---

## 📁 Folder Structure (Please Follow)

Each contribution should be organized similarly to `examples/`:

```
community/
└── <language_code>/
    └── <your_task_name>/
        ├── README.md               # Short explanation (in task language)
        ├── tasks/
        │   └── your_task.yaml
        └── data/
            └── your_dataset.csv
```

✅ This helps others use your task immediately by copying into their working `tasks/` and `data/` directories.

---

## 🚀 How to Submit

You can submit your contribution in two ways:

1. 📦 **Pull Request**  
   Fork the repository and create a PR with your files in the `community/` directory.

2. 📨 **GitHub Issue**  
   Open an issue and attach or link to your files (we'll help you integrate them).

---

## 📌 Tips

- Use clear names and folder structure
- Add a `README.md` inside your task folder describing:
  - The goal of the analysis
  - Expected labels (if classification)
  - Any special considerations

---

## 📚 Need Help?

See [`examples/`](../examples/) or read the  
📘 [YAML Task Guide](../docs/YAML_TASK_GUIDE.md) and  
🛠️ [YAML Tutorial](../docs/YAML_TUTORIAL.md)

---

Together we can build a powerful, flexible library of website understanding tools! 🌐🤖