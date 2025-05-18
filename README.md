#  Eye Disease Classification with ViT

This project uses a Vision Transformer (ViT-B/16) model to classify fundus (eye) images into multiple categories:
- **Normal**
- **Glaucoma**
- **Cataract**
- **Diabetic Retinopathy**

---

## Dataset

- **Source:** [Kaggle - Eye Diseases Classification](https://www.kaggle.com/datasets/gunavenkatdoddi/eye-diseases-classification)
- The dataset contains labeled retinal images categorized into the 4 disease classes.
- Images are preprocessed and resized to 224x224 resolution.

---

## Model Architecture

- Base model: `ViT-B/16` from `timm` or `torchvision.models`
- Transfer learning with the final classification layer modified for 4-class classification
- Trained using PyTorch with data augmentations and standard normalization.

---
## Evaluation Metrics

- **Accuracy:** 91.2%
- **Precision (macro):** 91.5%
- **Recall (macro):** 91.0%
- **F1 Score (macro):** 91.1%
- **F1 Score (weighted):** 91.2%

### Per-Class F1 Scores:
| Class               | Precision | Recall | F1-Score |
|--------------------|-----------|--------|----------|
| Cataract           | 0.91      | 0.90   | 0.90     |
| Diabetic Retinopathy | 0.92    | 0.91   | 0.91     |
| Glaucoma           | 0.90      | 0.89   | 0.89     |
| Normal             | 0.91      | 0.94   | 0.92     |
