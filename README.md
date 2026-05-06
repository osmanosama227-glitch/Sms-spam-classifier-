# 🛡️ SMS Spam Classifier — Interactive GUI

![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=flat&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat&logo=jupyter&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat)

> **Data Mining Assignment #1** — Egyptian Chinese University  
> An interactive Jupyter-based GUI that classifies SMS messages as **Spam** or **Ham** using three ML models with TF-IDF feature engineering and GridSearchCV optimization.

---

## 📸 Preview

![GUI Preview](preview.png)
> *Run all cells and the interactive GUI appears at the bottom of the notebook.*

---

## ✨ Features

- 🤖 **3 ML Models** — Naive Bayes, Logistic Regression, KNN
- 🔠 **TF-IDF Vectorization** with bigrams (1,2-gram range, top 5000 features)
- ⚙️ **GridSearchCV + 5-Fold Stratified CV** for hyperparameter tuning
- 🎨 **Fully interactive GUI** built with `ipywidgets` — no external app needed
- 📊 **Live model comparison** — accuracy, precision, F1, confusion matrix
- 🏆 **Auto-selects best model** based on F1 score
- 💬 **Sample messages** to test instantly

---

## 📂 Project Structure

```
sms-spam-classifier/
├── SMS_Spam_Classifier_GUI_4_1.ipynb   # Main notebook with GUI
├── spam.csv                             # Dataset (download separately)
├── requirements.txt                     # Python dependencies
└── README.md
```

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/sms-spam-classifier.git
cd sms-spam-classifier
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Download the dataset

Download `spam.csv` from Kaggle and place it in the same folder as the notebook:

🔗 [SMS Spam Collection Dataset — Kaggle](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset)

> The notebook also supports placing `archive.zip` in the same folder — it will auto-extract.

### 4. Run the notebook

```bash
jupyter notebook SMS_Spam_Classifier_GUI_4_1.ipynb
```

Then press **Ctrl+Shift+P → "Run All"** — the GUI will appear at the bottom.

---

## 🧠 Models & Methodology

| Model | Tuned Hyperparameters |
|---|---|
| Naive Bayes | `alpha` ∈ {0.01, 0.1, 0.5, 1.0, 2.0} |
| Logistic Regression | `C` ∈ {0.01, 0.1, 1, 10, 100}, solver ∈ {lbfgs, liblinear} |
| KNN | `k` ∈ {3, 5, 7, 11}, metric ∈ {euclidean, cosine}, weights ∈ {uniform, distance} |

**Pipeline:**
1. Text cleaning — lowercase, remove punctuation, strip stop words
2. TF-IDF vectorization (unigrams + bigrams, top 5000 features)
3. 80/20 train-test split (stratified)
4. GridSearchCV with 5-Fold Stratified CV (optimizing F1)
5. Evaluation — Accuracy, Precision, F1, Confusion Matrix

---

## 📊 Dataset

**SMS Spam Collection** — UCI Machine Learning Repository  
- 5,572 SMS messages labeled as `ham` (legitimate) or `spam`
- ~13.4% spam rate

---

## 🛠️ Tech Stack

- **Python 3.8+**
- `pandas`, `numpy` — data handling
- `scikit-learn` — ML models, TF-IDF, GridSearchCV
- `matplotlib`, `seaborn` — visualizations
- `ipywidgets` — interactive GUI

---

## 👤 Author

**Osman Osama**  
Data Science Student — Egyptian Chinese University  
Founder, [Data Wizards Community](https://github.com/osmanosama227-glitch)

---

## 📄 License

This project is licensed under the MIT License.

