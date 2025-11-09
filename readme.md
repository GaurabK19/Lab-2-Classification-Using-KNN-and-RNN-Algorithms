## Purpose
This lab explores the performance of two neighborhood-based classifiers, **K-Nearest Neighbors (KNN)** and **Radius Neighbors (RNN)**, using the Wine dataset from `sklearn`.  
The goal is to understand how changing key parameters — the number of neighbors (`k`) for KNN and the radius for RNN — affects model accuracy, and to determine the most effective settings for classification.

---

## Key Findings
- **KNN:**  
  - Accuracy improves as `k` increases up to a certain point, then levels off.  
  - Optimal performance was achieved at `k = 11`, balancing sensitivity to noise and generalization.

- **RNN:**  
  - Accuracy is sensitive to the radius parameter.  
  - Mid-range values around 450–500 produced the best results, while very small or very large values reduced performance.

- **Comparison:**  
  - KNN showed more consistent performance across different parameters.  
  - RNN can adapt to variations in local data density but requires careful tuning.  
  - Overall, KNN is more robust for this dataset, while RNN may be useful when local clustering patterns matter.

---

## Challenges and Decisions
- Choosing radius values for RNN required trial and error, as inappropriate values led to inaccurate predictions.  
- Feature standardization was necessary because both models are sensitive to distance metrics.  
- Ensured proper code structure and indentation to avoid runtime errors and maintain readability.

---

## Conclusion
This lab demonstrates how hyperparameters impact KNN and RNN performance.  
KNN provides stable and reliable accuracy, while RNN offers flexibility for datasets with uneven densities but needs careful radius selection.  