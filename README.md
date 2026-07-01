<div align="center">

# 🎓 AI-Based Student Performance Analysis System

### 🤖 Fine-Tuned LLM (Qwen2.5-3B-Instruct + LoRA) for Intelligent Student Performance Evaluation

<p align="center">
Analyze academic progression using Artificial Intelligence instead of simple mark comparison.
</p>

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![LLM](https://img.shields.io/badge/LLM-Qwen2.5--3B-success)
![LoRA](https://img.shields.io/badge/Fine--Tuning-LoRA-orange)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

</div>

---

## 📖 Overview

Traditional student evaluation systems simply compare marks.

This project leverages a **fine-tuned Large Language Model (LLM)** to intelligently analyze student academic progression between **Mid-Semester** and **End-Semester** examinations.

Instead of only calculating score differences, the AI understands performance trends and generates **human-like academic verdicts** explaining whether a student has improved, declined, or maintained performance.

> ⚠️ **Model weights (~2.5GB) are NOT included in this repository.**
> See the **Model** section below for reproduction instructions.

---

# ✨ Features

✅ AI-generated performance verdicts

📈 Subject-wise performance trend analysis

📊 Mid Semester vs End Semester comparison

🧠 Fine-tuned Qwen2.5-3B-Instruct model

⚡ LoRA fine-tuning for efficient training

📝 Structured CSV output

🚫 Handles missing values and incomplete records

💻 Lightweight inference pipeline

📂 Easy-to-use CSV input format

---

# 🏗️ System Workflow

```text
          Mid Semester CSV
                  │
                  ▼
        Data Preprocessing
                  │
                  ▼
        Subject-wise Comparison
                  │
                  ▼
      Fine-Tuned Qwen2.5-3B
          (LoRA Adapter)
                  │
                  ▼
      AI Performance Analysis
                  │
                  ▼
      Performance Verdict CSV
```

---

# 🧠 Model Information

| Property | Details |
|----------|---------|
| 🤖 Base Model | Qwen2.5-3B-Instruct |
| 🎯 Fine-Tuning | LoRA (Low Rank Adaptation) |
| 💻 Training Platform | Google Colab (T4 GPU) |
| 🧩 Framework | Hugging Face Transformers |
| ⚡ PEFT | Yes |
| 📦 Quantization | Optional (4-bit/8-bit) |

### Why Qwen?

✔ Excellent instruction following

✔ Strong reasoning capability

✔ Low hallucination rate

✔ Efficient inference

✔ Ideal for limited GPU environments

---

# 📂 Repository Structure

```text
AI-Student-Performance-Analysis/
│
├── finetuning/             # LoRA training scripts
├── training_inputs/        # Training datasets
├── testing_inputs/         # Testing datasets
├── outputs/                # Generated output CSVs
├── docs/                   # Project documentation
├── requirements.txt
└── README.md
```

---

# 📥 Input Format

The system requires **two CSV files**.

## 📄 mid.csv

| StudentID | Name | Math_Mid | English_Mid | Science_Mid | History_Mid |
|-----------|------|----------|--------------|--------------|-------------|

---

## 📄 end.csv

| StudentID | Name | Math_End | English_End | Science_End | History_End |
|-----------|------|----------|--------------|--------------|-------------|

### Missing Values

Use

```
NA
```

for unavailable marks.

Marks should be between

```
0 - 100
```

---

# 📤 Output

The model generates a structured CSV containing:

- 📈 Subject-wise improvement
- 📉 Subject-wise decline
- ❓ Missing subject detection
- 📊 Performance delta
- 🤖 AI-generated performance verdict
- 📝 Human-readable reasoning

Example:

| Student | Verdict |
|----------|----------|
| John | Excellent improvement across STEM subjects. Consistent academic growth observed. |
| Alice | Slight decline in Mathematics. Stable overall performance. |

---

# ⚙️ Installation

Clone the repository

```bash
git clone https://github.com/<your-username>/student-performance-analysis.git
```

Move into the project

```bash
cd student-performance-analysis
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

# 🚀 Usage

## Fine-Tune the Model (Optional)

Requires GPU

```bash
python finetuning/train.py
```

---

## Run Inference

```bash
python inference.py \
    --mid testing_inputs/mid.csv \
    --end testing_inputs/end.csv
```

---

# 📊 Technologies Used

| Technology | Purpose |
|------------|---------|
| 🐍 Python | Programming Language |
| 🤗 Hugging Face | Model Training |
| 🧠 Qwen2.5-3B | Base LLM |
| ⚡ LoRA | Parameter Efficient Fine-Tuning |
| 📊 Pandas | Data Processing |
| 📄 CSV | Dataset Format |
| ☁️ Google Colab | Training Environment |

---

# 📚 Documentation

Complete project documentation is available in

```
docs/
```

The report includes

- 📖 Literature Survey
- 🏗️ System Architecture
- 🧹 Data Preprocessing
- 🧠 Model Fine-Tuning
- 📊 Evaluation Metrics
- 📈 Results
- 🔮 Future Scope

---

# ⚠️ Model

The fine-tuned model checkpoint is **not included** because its size is approximately **2.5 GB**.

To reproduce the model:

1. Prepare your dataset.
2. Run scripts inside:

```
finetuning/
```

3. Train using LoRA on **Qwen2.5-3B-Instruct**.

You may also host the trained adapter on:

- 🤗 Hugging Face Hub
- ☁️ Google Drive

and include the download link here.

---

# 🚀 Future Improvements

- 📊 Interactive dashboard
- 🌐 Flask Web Interface
- 📈 Visualization graphs
- 🎯 Multi-semester analysis
- 🧠 RAG integration
- 📄 PDF report generation
- ☁️ Hugging Face deployment
- 🌍 Multi-language support

---

# 👨‍💻 Author

**<Your Name>**

LinkedIn: *Add your profile*

GitHub: *Add your profile*

---

<div align="center">

### ⭐ If you found this project useful, don't forget to give it a Star ⭐

Made with ❤️ using **Python, Hugging Face, LoRA and Qwen2.5-3B**

</div>
