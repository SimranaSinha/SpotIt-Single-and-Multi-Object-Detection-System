# Milestone 1 — Object Identification & Deep Learning Model Evaluation

This project focuses on building a custom image dataset around a single real-world object and evaluating multiple deep learning models to determine the most suitable approach for object recognition.

---

📌 Project Objectives

This milestone consists of two main components:

1️⃣ Unique Object Dataset Creation (Individual Task)

Each student was required to:
- Identify one unique physical object
- Generate at least 100 images of that object
- Ensure variation in:

  - 	Angles
  - 	Lighting conditions
  - 	Backgrounds
  - 	Distance and orientation
  - 	Upload all images to the shared group folder

This step ensures dataset diversity, which is essential for training robust computer vision models.

2️⃣ Deep Learning Model Development 
- Combined all individual object datasets
- Prepared and organized the dataset for training
- Implemented and tested multiple deep learning models
- Compared performance across models
- Identified the best-performing model for this dataset

---

🧠 Models Evaluated

The following deep learning approaches were tested:
- Convolutional Neural Networks (CNN-based models)
- Transfer Learning models (pretrained architectures)
- Custom architectures where applicable

Each model was trained and evaluated under the same conditions for fair comparison.

---

📊 Evaluation Metrics

Model performance was measured using:
- Accuracy
- F1-Score
- Confusion Matrix
- Classification Report

These metrics helped assess both overall performance and class-level behavior.

---

🏆 Best Model Selection

The final model was chosen based on:
- Highest test accuracy
- Strong macro F1-score
- Balanced performance across classes
- Stable training behavior (no overfitting or instability)

The selected model is the most suitable for this dataset and object recognition task.

---

📊 Model Performance Summary

- The following table shows the performance of all deep learning models evaluated on the dataset.

| Model Name           | Validation Accuracy | Test Accuracy | Test F1 Score (Macro) |
|----------------------|---------------------|---------------|-----------------------|
| SimpleCNN            | 62.01%              | 60.45%        | 57.66%                |
| ResNet18             | 99.68%              | 98.87%        | 98.84%                |
| MobileNetV3Small     | 97.24%              | 96.76%        | 96.73%                |

---

🏆 Best Performing Model

- ResNet18 achieved the highest accuracy and F1 score, showing strong generalization and balanced class performance. It was selected as the final model for this dataset.

---

📌 Metrics Used
- Validation Accuracy – Performance during training to monitor overfitting
- Test Accuracy – Final performance on unseen data
- F1 Score (Macro) – Balance between precision and recall across all classes

---

📁 Repository Contents
- Dataset (generated object images)
- Training and evaluation code
- Model performance results
- Confusion matrices and reports
- Final analysis of model comparison

---

🎯 Key Learning Outcomes
- Building a custom computer vision dataset
- Understanding how data diversity impacts model performance
- Applying deep learning for image classification
- Comparing multiple architectures for the same task
- Selecting models based on metrics, not assumptions

---

This milestone establishes the foundation for more advanced object detection and multi-object tasks in later phases.

