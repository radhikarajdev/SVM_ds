# Optimized SVM Evaluation

This project evaluates the performance of an **Optimized Support Vector Machine (SVM)** on different data samples by tuning its hyperparameters. The results are compared based on classification accuracy and convergence behavior.

---

## 🧠 Methodology

The goal is to assess the performance of SVMs across 10 different dataset samples by identifying the best hyperparameters for each.

### Steps:

1. **Dataset Sampling**:
   - The original dataset was divided into 10 unique samples: S1 through S10.

2. **SVM Training**:
   - An SVM with an RBF (Radial Basis Function) kernel was used.
   - The hyperparameters `nu` and `gamma` were optimized using either grid search or random search.

3. **Evaluation**:
   - Accuracy was used as the primary evaluation metric.
   - The best accuracy and corresponding hyperparameters were recorded for each sample.

4. **Convergence Monitoring**:
   - Optimization progress was monitored over iterations to ensure convergence and performance stability.

---

## 📊 Results

### 🔹 Table 1: Comparative Performance of Optimized-SVM

| Sample | Best Accuracy | Best Parameters (Kernel, Nu, Gamma) |
|--------|----------------|--------------------------------------|
| S1     | 0.8015         | rbf, 0.2942, auto                   |
| S2     | 0.7836         | rbf, 0.3382, scale                  |
| S3     | 0.7903         | rbf, 0.3709, scale                  |
| S4     | 0.7861         | rbf, 0.348, auto                    |
| S5     | 0.7938         | rbf, 0.335, auto                    |
| S6     | 0.8019         | rbf, 0.3345, scale                  |
| S7     | 0.7928         | rbf, 0.3432, scale                  |
| S8     | 0.7959         | rbf, 0.3135, scale                  |
| S9     | 0.7618         | rbf, 0.4, scale                     |
| S10    | 0.8005         | rbf, 0.2695, auto                   |

> ✅ **Highest Accuracy:** Sample **S6** with **0.8019**

---

## 📈 Convergence Graph

### Figure 1: Convergence of Best SVM (Sample S6)

![Convergence Graph](graph.png)

- The graph shows how accuracy evolves over 100 iterations during the optimization process for Sample S6.
- The optimizer quickly improves accuracy in the early stages and stabilizes after around 30 iterations.
- The final accuracy converges to **0.8019**, showing a stable and effective tuning process.

---

## 📁 Files

- `SVM_ds.ipynb`: Jupyter Notebook containing the training, optimization, and evaluation code.
- `README.md`: This documentation file.
- Images:
  - `table.png` (Result Table)
  - `graph.png` (Convergence Graph)

---

## 📌 Notes

- All experiments were conducted using the RBF kernel.
- Gamma was set to either `scale` or `auto` based on which yielded the best accuracy per sample.
- Optimizer convergence was visualized to confirm stability and optimality of the selected parameters.

---

## 🧪 Future Work

- Try other kernels (e.g., polynomial or sigmoid).
- Explore multi-class classification or regression scenarios.
- Implement more advanced optimization algorithms (e.g., Bayesian Optimization, Genetic Algorithms).

---

## 📬 Contact

For any questions or feedback, feel free to open an issue or reach out.

