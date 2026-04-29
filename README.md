# Road Surface Classification
 
> Solution developed for the **Voxar Labs** technical challenge, which proposes classifying road surface images into three categories: **Asphalt**, **Belgian Blocks**, and **Off-road**.
 
---
 
## 📋 About the challenge
 
The goal was not to maximize performance, but to demonstrate the ability to:
 
- Structure a computer vision problem
- Develop an initial viable solution
- Critically investigate results
- Communicate decisions clearly
The dataset is real, **highly imbalanced**, and includes challenging visual conditions — lighting variations, rain, nighttime periods, and different capture devices.
 
---
 
## 🧠 Approach
 
The solution is based on **Transfer Learning** with the **ResNet18** architecture pre-trained on ImageNet, chosen for its efficiency and strong performance on classification tasks with moderate-sized datasets.
 
---
 
## 📁 Notebook structure
 
The `road_classification.ipynb` file consolidates the entire solution — both the technical documentation and the code — following the format required by the challenge brief. It is organized into the following sections:
 
| # | Section | Description |
|---|---------|-------------|
| 1 | **Approach overview** | Model description, justification, and libraries used |
| 2 | **Problem understanding** | Initial dataset analysis and expected challenges |
| 3 | **Preprocessing and data loading** | Input transformations and class distribution analysis |
| 4 | **Training and evaluation pipeline** | Reusable structure shared across all experiments |
| 5 | **Baseline** | Model with fine-tuning only on the final layer, no class imbalance handling |
| 6 | **Experiment 1 — Class Weights** | Hypothesis: penalizing majority classes improves recall on minority ones |
| 7 | **Experiment 2 — Fine-Tuning** | Hypothesis: unfreezing deeper layers increases domain adaptation capacity |
| 8 | **Experiment 3 — Data Augmentation** | Hypothesis: synthetic variations reduce overfitting and improve generalization |
| 9 | **Model comparison** | Consolidated metrics table across all experiments |
| 10 | **Critical analysis** | Where the approach worked, where it failed, and next steps |
| 11 | **Tool usage** | Transparency on the use of LLMs throughout the process |
 
---
 
## 🛠️ Tech stack
 
| Library | Usage |
|---------|-------|
| `torch` / `torchvision` | Model, training, and data loading |
| `scikit-learn` | Metrics and confusion matrix |
| `matplotlib` / `seaborn` | Visualizations |
