# 📊 Predictive Analytics SVM Optimization Assignment

This repository contains the implementation and results of an SVM optimization assignment for the subject **Predictive Analytics using Statistics of Data Science**.

---

## 🧠 Objective

To evaluate the performance of Support Vector Machine (SVM) classifiers on a multi-class dataset from the UCI Machine Learning Repository. The goal is to:
- Perform 10 random train-test splits (70-30).
- Optimize the SVM model across 100 iterations per sample.
- Record the best parameters and accuracy.
- Visualize the convergence graph for the best performing sample.

---

## 📚 Dataset Used

**Letter Recognition Dataset**  
- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/letter+recognition)  
- **Classes**: 26 (A-Z)  
- **Samples**: 20,000+  
- **Attributes**: 16 numerical features

---

## 🔍 Methodology

1. **Data Preprocessing**
   - Loaded dataset and labeled target variable.
   - Scaled features using StandardScaler.
   - Encoded labels using LabelEncoder.

2. **Sampling Strategy**
   - 10 different samples using random `train_test_split` (70-30).

3. **Model Optimization**
   - For each sample:
     - Randomly searched over the following parameters:
       - Kernels: `linear`, `poly`, `rbf`, `sigmoid`
       - C values: `0.1`, `1`, `10`
       - Gamma: `scale`, `auto`
     - Trained the model over 100 iterations and recorded best parameters and accuracy.

4. **Evaluation**
   - Accuracy used as the fitness metric.
   - A convergence graph was plotted for the best sample.

---

## 📦 Requirements

Install the following Python packages before running the code:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn tqdm
