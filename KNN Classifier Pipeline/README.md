# 🧠 KNN Evaluation Summary

This project evaluates the stability and performance of a **K-Nearest Neighbors (KNN)** classifier on a dataset of **569 samples** with **30 numeric features**.  
All features were **Min-Max scaled** and labels encoded to ensure balanced distance calculations.

---

## **Methodology**
- **10-fold stratified cross-validation** repeated over **100 randomized trials** to reduce variance.  
- Tested **k values from 1 to 10**, tracking both **accuracy** and **macro-averaged F1**.  
- Low standard deviation confirmed strong consistency across runs.

---

## **Results**
- Accuracy and F1 remained consistently high with only minor fluctuations.  
- **k = 7** achieved the best overall balance between accuracy, F1, and stability.  
- The experiment validated KNN’s reliability as a **robust baseline model** for diagnostic tasks.

---

## **Limitations & Future Work**
- KNN’s performance depends on the chosen **distance metric**; Euclidean may degrade in high-dimensional data.  
- Future work could explore:
  - Alternative distance metrics  
  - Distance-weighted voting  
  - Comparisons with other classifiers  

---
