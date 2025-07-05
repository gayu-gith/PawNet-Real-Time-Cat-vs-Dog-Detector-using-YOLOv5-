# PawNet-Real-Time-Cat-vs-Dog-Detector-using-YOLOv5-
# 🐶🐱 Cat vs Dog Detection using YOLOv5

This project demonstrates a deep learning-based **object detection system** that can accurately distinguish between **cats** and **dogs** in images. The model is built using **YOLOv5**, trained on a custom dataset annotated and processed using **Roboflow**, and executed in **Google Colab**.

---

## 📌 Project Objective

The aim is to create a real-time image detection model capable of identifying cats and dogs in visual data. This includes:
- Training a custom YOLOv5 object detection model
- Preprocessing and managing datasets using Roboflow
- Evaluating model performance on test images
- Performing inference to draw bounding boxes and labels on detected animals

---

## 🔧 Technologies Used

| Tool            | Purpose                                   |
|-----------------|--------------------------------------------|
| YOLOv5          | Object Detection Framework                 |
| Roboflow        | Dataset preparation & annotation           |
| Google Colab    | Training and inference (GPU acceleration)  |
| PyTorch         | Deep learning backend                      |
| OpenCV & PIL    | Image preprocessing and visualization      |
| Python          | Programming language                       |

---

## 🗃️ Dataset

### ✅ Sources:
- **Oxford-IIIT Pet Dataset** (from Kaggle)
- **Custom annotations and dataset preparation** via [Roboflow](https://roboflow.com)

### ✅ Classes:
- `Cat`
- `Dog`

Dataset was preprocessed into YOLOv5-compatible format and included:
- Annotated training images
- Bounding box labels
- Separate `train`, `valid`, and `test` splits

---

## 🏋️ Model Training

The model was trained on Google Colab using YOLOv5's training script:

```bash
!python train.py \
  --img 416 \
  --batch 16 \
  --epochs 10 \
  --data {dataset.location}/data.yaml \
  --weights yolov5s.pt \
  --name pets_detector_10epochs 
```
## 📸 Sample Output

The trained YOLOv5 model successfully detects cats and dogs in a variety of test images. Below are some sample results:

### 🔍 Detection Example 1

[Dog Detected]

![image](https://github.com/user-attachments/assets/a9c396fc-0263-4e65-af28-e12807a6f551)

> 🐶 Detected: **Dog**  
> 📏 Confidence: **94.3%**  
> 📍 Bounding box drawn in blue

---

### 🔍 Detection Example 2

[Cat Detected]

![image](https://github.com/user-attachments/assets/2a2727a4-38c0-4647-afbc-bade86a3cc70)

> 🐱 Detected: **Cat**  
> 📏 Confidence: **91.8%**  
> 📍 Bounding box drawn in green

---

### ⚙️ Output Directory

All inference results are automatically saved in:



