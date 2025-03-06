# 📈 Batch Summary Performance Evaluation

This project evaluates and compares text summarization models' performance using **ROUGE** and **BERTScore** metrics. It systematically analyzes multiple summaries, compares them against reference summaries (GPT-generated and Cosine Similarity-based), and exports detailed performance metrics to an Excel file.

---

🔗 Related Projects This project is part of a modular research framework for evaluating and improving fairy tale summarization models. Below are the related repositories:

| Children's Tale Summarizer - Flask App | The main Flask-based API that generates fairy tale summaries. (https://github.com/SinemCiftciDemirci/childrens-tale-summarizer-flask-app) |

| GPT Summarizer | Creates GPT-based fairy tale summaries. (https://github.com/SinemCiftciDemirci/gpt-summarizer) |

| Cosine Similarity Summarizer | Performs extractive summarization using cosine similarity. (https://github.com/SinemCiftciDemirci/cosine-similarity-summarizer) |

| Single Summary Evaluation | Measures the performance of a single summary using BERTScore and ROUGE score. (https://github.com/SinemCiftciDemirci/single-summary-evaluation) |

| Batch Summary Performance Evaluation | Compares model-generated summaries with GPT and Cosine-based reference summaries, calculating ROUGE and BERTScore collectively. (https://github.com/SinemCiftciDemirci/batch-summary-performance-evaluation) |

| Summary Performance Comparison | Creates visual performance comparisons from the Model_Performance.xlsx file produced in the Batch Summary Evaluation repo. (https://github.com/SinemCiftciDemirci/summary-performance-comparison) |

| Vision Model Test | Translates the generated summaries into English and creates three visuals: introduction, development, and conclusion. (https://github.com/SinemCiftciDemirci/vision-model-test) |

Each repository serves a unique role in evaluating or improving summarization models. You can use them individually or together for deeper analysis.

## 🚀 Key Features

- **Automated matching** of model-generated summaries with corresponding reference summaries.
- **Calculates detailed evaluation metrics:**
  - ✅ **ROUGE-1, ROUGE-2, ROUGE-L**
  - ✅ **BERTScore (Precision, Recall, F1)** with Turkish language support
- **Easy-to-understand Excel reports** for performance comparison.

---

## 📂 Project Structure

```
performance-evaluation/
├── performance.py
├── summaries/
├── gpt_summaries/
├── cos_sim_summaries/
├── metrics/
│   └── Model_Performance.xlsx
├── README.md

```

---

## 📌 Installation

First, install the required Python libraries:

```bash
pip install rouge bert-score tqdm pandas openpyxl
```

---

## 🎯 How to Use

### 1. Prepare your summaries

- Place your model-generated summaries in the `summaries` folder.
- Ensure GPT-generated summaries are in the `gpt_summaries` folder.
- Ensure Cosine Similarity-based summaries are in the `cos_sim_summaries` folder.

### 2. Run the evaluation script

Execute the script with:

```bash
python performance.py
```

The script will:
- Match each model-generated summary with corresponding reference summaries.
- Compute the evaluation metrics automatically.

### 3. Review the results

The results will be saved automatically to:

```
metrics/Model_Performance.xlsx
```

---

## 🛠️ Evaluation Metrics Explained

- **ROUGE scores** evaluate the lexical overlap (words and phrases) between model and reference summaries.
- **BERTScore** provides a semantic similarity measure, particularly effective with the multilingual model **`xlm-roberta-base`**, making it suitable for Turkish language evaluation.

---

## 🔧 Troubleshooting

- Ensure folder structures and file names follow the expected format.
- Check terminal output for errors or unmatched files.
- Confirm all Python libraries are correctly installed.

---

## 📜 License

This project is licensed under the MIT License. Feel free to use, modify, and distribute.

