# 🔢 Digit Recognition — ML Model Comparison

> Handwritten digit classification on the MNIST dataset using classical ML algorithms.  
> Comparing **Logistic Regression**, **Naive Bayes (MNB)**, and **SVM (RBF kernel)**.

---

## 📊 Live Dashboard

**[→ View Interactive Model Comparison Dashboard](https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/visualizer.html)**

> Replace the link above after enabling GitHub Pages (Settings → Pages → Deploy from `main` branch).

---

## 🏆 Results Summary

| Model | Accuracy | F1 Score (macro) | Train Time |
|-------|----------|-----------------|------------|
| Logistic Regression | 91.8% | 0.917 | ~18s |
| Naive Bayes (MNB) | 82.4% | 0.821 | ~0.4s |
| **SVM (RBF kernel)** | **97.9%** | **0.979** | ~210s |

---

## 📁 Project Structure

```
digit-recognition/
├── train.csv               # Kaggle MNIST training data (42,000 samples)
├── digit_recognizer_ml.ipynb  # Main notebook
├── visualizer.html         # Interactive results dashboard
└── README.md
```

---

## 🚀 How to Run

```bash
# 1. Clone the repo
git clone https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
cd YOUR-REPO-NAME

# 2. Install dependencies
pip install pandas numpy scikit-learn

# 3. Download dataset from Kaggle
# https://www.kaggle.com/competitions/digit-recognizer/data
# Place train.csv in the root directory

# 4. Open the notebook
jupyter notebook digit_recognizer_ml.ipynb
```

---

## 🧠 Key Insight

**Why does Naive Bayes underperform?**

Multinomial NB assumes each pixel feature is **conditionally independent** given the class.
But in digit images, adjacent pixels are highly correlated — a dark pixel at (14,14) strongly
implies darkness at (14,15). Violating this independence assumption strips away critical
spatial structure, causing ~15% lower accuracy than SVM.

SVM with an RBF kernel captures nonlinear pixel relationships **without** that assumption —
hence its dominance on image data.

---

## 📦 Tech Stack

![Python](https://img.shields.io/badge/Python-3.10-3776AB?style=flat&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Kaggle](https://img.shields.io/badge/Dataset-MNIST-20BEFF?style=flat&logo=kaggle&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat&logo=jupyter&logoColor=white)

---

## 👤 Author

**Lalith** · [GitHub](https://github.com/lalitheswar09-data)

---

## ⚙️ Enable GitHub Pages (to activate the dashboard link)

1. Go to your repo → **Settings** → **Pages**
2. Under *Source*, select **Deploy from a branch**
3. Choose `main` branch, `/ (root)` folder → **Save**
4. Your dashboard will be live at:  
   `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/visualizer.html`
