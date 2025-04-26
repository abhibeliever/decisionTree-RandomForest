# decisionTree-RandomForest
Used Decision Tree And Random Forest Technique


## Model Comparison

### Decision Tree vs Random Forest

| Aspect                     | Decision Tree                                      | Random Forest                                                      |
|----------------------------|----------------------------------------------------|--------------------------------------------------------------------|
| **Definition**             | A tree-structured model that splits data based on feature thresholds to predict a target. | An ensemble of many decision trees, each trained on a bootstrap sample and random subset of features. |
| **Ensemble?**              | No – it’s just one tree.                           | Yes – typically dozens to hundreds of trees.                        |
| **Randomness**             | Deterministic splits (given same data & hyper-params). | Two sources of randomness:  
1. Bootstrap sampling of training rows (bagging)  
2. Random subset of features considered at each split. |
| **Bias vs. Variance**      | Low bias, high variance → prone to overfitting.    | Slightly higher bias than a single tree but much lower variance → better generalization. |
| **Overfitting**            | Easily overfits if tree is deep or unpruned.       | Robust to overfitting—averaging trees reduces noise.               |
| **Interpretability**       | Very interpretable—you can trace each decision path. | Harder to interpret as a whole (individual trees are interpretable, but not the forest aggregate). |
| **Accuracy**               | Good on simple problems, but can be brittle.       | Generally higher and more stable accuracy across datasets.         |
| **Training Time**          | Fast.                                              | Slower (training many trees), but embarrassingly parallelizable.    |
| **Prediction Time**        | Very fast (just traverse one tree).                | Slower than one tree (must traverse each tree and average/vote).   |
| **Key Hyperparameters**    | `max_depth`, `min_samples_split`, `criterion` (gini/entropy) | `n_estimators`, `max_features`, `max_depth`, `min_samples_leaf`, `bootstrap` |
| **When to use**            | - Quick, interpretable model  
- Small or low-complexity data | - Predictive performance is paramount  
- Sufficient compute to train multiple trees |

