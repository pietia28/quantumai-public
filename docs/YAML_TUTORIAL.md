# 🛠️ Step-by-Step Tutorial: Creating Your First Task YAML (QuantumAI CLI)

This tutorial will walk you through building a working `task.yaml` file for **QuantumAI CLI**, using a simple use case: identifying if a company is a potential client based on website text.

---

## 🧾 What You’ll Need

- Basic understanding of what you want to detect (classification problem)
- A few labeled examples saved in a `.csv` file
- A YAML editor (or just any text editor like VSCode or Notepad++)

---

## 🧠 Step 1: Define the Goal

We want to answer the question:

> "Is this company a potential client?"  
So the output should be either `yes` or `no`.

---

## 🧱 Step 2: Create Training Data (`data/potential_client.csv`)

Create a file like this:

```csv
content,label
We offer automation systems for buildings,yes
We are a public university focused on education,no
Smart home devices for energy efficiency,yes
Official municipal government portal,no
```

Save it under: `data/potential_client.csv`

---

## 🧩 Step 3: Build the YAML Task

Create a new file: `tasks/potential_client.yaml`

```yaml
task_name: potential_client
description: Detect if a company is a potential client
type: classification

input_column: content
output_column: label

model: LogisticRegression
vectorizer: tfidf

data_file: data/potential_client.csv

output_format:
  - field: url
    from: page.url
  - field: prediction
    from: prediction
  - field: score
    from: probability
  - field: keywords
    from: keywords

report_template: |
  ### {url}
  - **Prediction**: {prediction}
  - **Confidence**: {score:.2f}%
  - **Important keywords**: {keywords}
```

---

## 🔍 Step 4: Analyze a Website

Use the following command to run the analysis:

```bash
quant analyze --url https://example.com --task tasks/potential_client.yaml -o client_report
```

---

## ✅ Step 5: Read the Output

Check the file `analysis_client_report_example.com_<timestamp>.md`  
You’ll see a report like:

```
### https://example.com
- Prediction: yes
- Confidence: 81.34%
- Important keywords: smart, automation, energy
```

---

## 🧪 Bonus: Train the model manually

```bash
quant train --task tasks/potential_client.yaml
```

This will train and save the model in your `.quantumai/models/` folder.

---

## 💡 Tips

- Always keep your CSV and YAML in sync (column names!)
- You can customize the report format using `{}` placeholders
- Use real data for better results (10–50+ examples recommended)

---

Need help? Post an issue or example in the community folder or GitHub.