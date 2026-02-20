# Milestone 2 — Multi-Object Identification & YOLO Dataset Preparation

This milestone extends the project from single-object recognition (Milestone 1) to **multi-object detection** using the YOLO framework.

The primary focus of this stage is to:

* Generate multi-object synthetic images
* Create accurate bounding box annotations
* Prepare a YOLO-compatible dataset
* Train and validate a detection model

---

## 🎯 Project Objectives

Milestone 2 consists of three major components:

### 1️⃣ Multi-Object Dataset Creation

* Generate 100+ synthetic images
* Randomly place multiple objects in a single image
* Apply scaling and positioning variation
* Introduce diversity in background and layout

### 2️⃣ Bounding Box Annotation

* Automatically compute bounding box coordinates
* Convert coordinates into YOLO normalized format
* Generate one label file per image

### 3️⃣ YOLO Dataset Configuration

* Organize images into train / validation folders
* Create `data.yaml` configuration file
* Define number of classes and class names
* Ensure consistent object ID mapping

---

## 📁 Dataset Structure

🔗 Google Drive Link:
https://drive.google.com/drive/folders/15Mnq3MJ09t81ZyLuBWz7eOeKhOqVnWrp?usp=sharing

The dataset follows YOLO directory formatting:

```
Output_Folder_YoLo/
│
├── 📄 data.yaml
│
├── 📁 images/
│   ├── 📁 train/
│   └── 📁 val/
│
├── 📁 labels/
│   ├── 📁 train/
│   ├── 📁 val/
│   ├── 📄 train.cache
│   └── 📄 val.cache
│
├── 📁 Test Files/
│   └── 📄 images
│
└── 📁 Group5/
    ├── 📁 Training/
    └── 📁 Validation/

```
Each image has a corresponding `.txt` label file with the same filename.

---

## 🏷 Annotation Format

YOLO normalized format was used:

```
class_id x_center y_center width height
```

Where:

* `class_id` → derived from folder/class mapping
* `x_center`, `y_center`, `width`, `height` → normalized between 0 and 1

This ensures compatibility with YOLO training pipelines.

---

## ⚙️ Implementation Workflow

### Step 1 — Image Generation

* Background canvas creation
* Random object placement
* Scaling variation
* Overlap control using IoU logic

### Step 2 — Bounding Box Calculation

* Extract object position
* Compute width & height
* Normalize coordinates
* Save annotation file

### Step 3 — Dataset Configuration

* Train/Validation split
* `data.yaml` creation
* Class definitions verified

---

## 📊 Model Training

YOLO was used to train the multi-object detection model.

### Training Process:

* Load dataset using `data.yaml`
* Train custom detection model
* Monitor training & validation loss
* Save best model weights

---

## 📈 Evaluation Metrics

The detection model was evaluated using:

* mAP (Mean Average Precision)
* Precision
* Recall
* F1 Score

These metrics evaluate both classification accuracy and bounding box localization performance.

---

## 🗂 Files Included

```
📁 Milestone 2/
│
├── 📄 Milestone2.ipynb  – Multi-object image generation and YOLO dataset preparation
│
├── 📄 data.yaml   – YOLO dataset configuration (classes, paths, splits)
│
├── 📄 Milestone_2_Group_5_Report.pdf  – Detailed milestone report with methodology and results
│
└── 📘  README.md  – Milestone documentation
```
---

## 🔎 Key Learnings

* Bounding box normalization is critical for YOLO performance
* Small annotation errors significantly reduce mAP
* Dataset diversity improves model robustness
* Folder-based class mapping simplifies object ID assignment
* Overlap control improves training stability

---

## ✅ Conclusion

Milestone 2 successfully transitions the project from classification to **multi-object detection**.

By the end of this milestone:

* A complete YOLO-compatible dataset was created
* Multi-object images were generated and labeled
* The detection model was trained and validated
* Object IDs and bounding boxes were predicted accurately

This milestone establishes the foundation for scalable object detection systems using custom synthetic datasets.

