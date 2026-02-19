# SpotIt – Single and Multi-Object Detection System

An end-to-end deep learning project focused on custom object identification and multi-object detection using synthetic dataset generation and YOLOv8.

This project progressively builds from single-object dataset creation to full multi-object detection with bounding box localization and model evaluation.

---

## Project Overview

The project is divided into structured milestones:

* **Milestone 1** – Object Identification & Deep Learning Model Evaluation
* **Milestone 2** – Multi-Object Dataset Generation & YOLO Annotation
* **Milestone 3** – Custom YOLOv8 Training & Detection 
* **Milestone 4** – Final Reporting

The goal is to design a complete object detection pipeline from dataset creation to model evaluation.

---

# Milestone 1 – Object Identification & Model Evaluation

This milestone focuses on building a custom dataset around a single real-world object and evaluating multiple deep learning models to determine the most suitable approach.

### Objectives

* Identify one unique physical object
* Generate at least 100 images
* Introduce variation in:

  * Angles
  * Lighting
  * Background
  * Orientation
* Train and compare deep learning models

### Work Completed

* Dataset creation (100+ images)
* Image preprocessing
* Data splitting (Train / Validation / Test)
* Model training and performance comparison
* Selection of best-performing model

### Key Learning

* Data diversity improves generalization
* Transfer learning outperforms training from scratch for small datasets
* Overfitting occurs quickly in limited datasets without augmentation

Files:

* `Milestone1 (Group5).ipynb`
* `Milestone_1_Group_5.pdf`
* `Milestone 1 README.md`

---

# Milestone 2 – Multi-Object Dataset & YOLO Labeling

This milestone extends the project to multi-object detection by generating synthetic images and preparing YOLO-format annotations.

### Objectives

* Generate 100+ multi-object images
* Random placement of objects
* Automatic bounding box generation
* Assign object ID based on folder name
* Save annotations in YOLO format

### Implementation Highlights

* Image compositing using PIL
* Random scaling and positioning
* IoU-based overlap control
* Normalized YOLO annotation format:

```
class_id x_center y_center width height
```

### Key Learning

* Proper bounding box normalization is critical
* Controlled randomness improves model robustness
* Label consistency directly impacts YOLO performance

Files:

* `Milestone2.ipynb`
* `Milestone 2 README.md`

---

# Milestone 3 – YOLOv8 Custom Training and Detecting

The final detection system was built using YOLOv8 for multi-object detection.

### Pipeline

* Dataset split (Train / Val / Test)
* Custom `data.yaml`
* YOLOv8 model training
* Performance evaluation

### Evaluation Metrics

* mAP (Mean Average Precision)
* Precision
* Recall
* F1 Score

### Results

* Successful object ID detection
* Accurate bounding box localization
* Stable performance across validation set
* Improved detection with augmentation

Files:

* `Training and Testing.ipynb`
* `Milestone 3 README.md`

---

# Technical Stack

* Python
* PyTorch
* YOLOv8 (Ultralytics)
* PIL (Image Processing)
* NumPy
* Google Colab

---

# Repository Structure

```
SpotIt-Single-and-Multi-Object-Detection-System/
│
├── Milestone 1/
│   ├── Milestone1 (Group5).ipynb
│   ├── Milestone_1_Group_5.pdf
│   ├── README.md
│
├── Milestone 2/
│   ├── Milestone2.ipynb
│   ├── Milestone_2_Group_5_Report.pdf
│   ├── README.md
│
├── Milestone 3/
│   ├── Training and Testing.ipynb
│
├── README.md   (Main Project Overview)
```

---

# Key Takeaways

* Building a clean dataset is as important as model selection
* Synthetic data generation can effectively train object detection models
* YOLO requires precise annotation formatting
* Folder-based class labeling simplifies ID mapping
* Model evaluation must consider both accuracy and localization performance

---

# Final Conclusion

This project demonstrates the full lifecycle of a custom object detection system:

1. Dataset creation
2. Model experimentation
3. Multi-object synthetic generation
4. YOLO training and evaluation

The system successfully detects and localizes objects with assigned IDs, showcasing practical implementation of deep learning-based object detection.



* Or tailor it for academic submission formatting

