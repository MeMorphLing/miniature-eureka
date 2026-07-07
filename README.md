# 🛣️ Road Lane Segmentation using U-Net (PyTorch)

An end-to-end deep learning project for **road lane segmentation** using **U-Net with a ResNet34 encoder** implemented in **PyTorch**. This notebook covers the complete semantic segmentation pipeline—from dataset loading and preprocessing to model training, evaluation, and prediction visualization.

---

## 📌 Project Overview

Road lane segmentation is a semantic segmentation task that identifies lane markings at the pixel level, enabling autonomous vehicles and Advanced Driver Assistance Systems (ADAS) to understand road boundaries accurately.

This project demonstrates the complete workflow of building a lane segmentation model using modern deep learning practices.

---

## ✨ Features

- 📥 Automatic dataset download from Kaggle
- 🖼️ Image and mask visualization
- 📊 Dataset statistics and analysis
- 🔄 Data preprocessing and augmentation
- ✂️ Train, Validation, and Test split
- 📦 Custom PyTorch Dataset and DataLoader
- 🧠 U-Net with ResNet34 encoder
- 🎯 BCE + Dice Loss
- 📈 IoU and Dice Score evaluation
- ⚡ GPU training support
- 💾 Model checkpointing
- 📉 Training history visualization
- 🔍 Prediction visualization on test images

---

# 📂 Project Pipeline

```
Dataset
      │
      ▼
Data Loading
      │
      ▼
Visualization
      │
      ▼
Preprocessing
      │
      ▼
Data Augmentation
      │
      ▼
Train / Validation / Test Split
      │
      ▼
PyTorch Dataset & DataLoader
      │
      ▼
U-Net (ResNet34 Encoder)
      │
      ▼
Training
      │
      ▼
Evaluation
      │
      ▼
Prediction & Visualization
```

---

# 🧠 Model Architecture

The project uses:

**U-Net**

with a

**ResNet34 Encoder (ImageNet Pretrained)**

### Why U-Net?

- Encoder-Decoder architecture
- Skip Connections for preserving spatial information
- Excellent performance for semantic segmentation
- Efficient for pixel-level classification tasks

---

# 📚 Technologies Used

- Python
- PyTorch
- OpenCV
- NumPy
- Matplotlib
- Albumentations
- segmentation-models-pytorch
- scikit-learn
- KaggleHub
- tqdm

---

# 📁 Project Structure

```
.
├── RoadLane_Segmentation.ipynb
├── checkpoints/
│   └── best_model.pth
├── dataset/
├── outputs/
│   ├── predictions/
│   └── visualizations/
└── README.md
```

---

# 📊 Dataset Preparation

The notebook includes:

- Loading the road lane dataset
- Image-mask pairing
- Data validation
- Dataset statistics
- Random sample visualization

---

# 🔄 Data Preprocessing

The preprocessing pipeline includes:

- Image resizing
- Mask resizing
- Normalization
- Tensor conversion

---

# 🎨 Data Augmentation

Implemented using **Albumentations**.

Examples include:

- Horizontal Flip
- Random Rotation
- Brightness & Contrast Adjustment
- Random Scaling
- Normalization

These augmentations improve model robustness and generalization.

---

# 🏗️ Model Configuration

| Component | Value |
|-----------|-------|
| Architecture | U-Net |
| Encoder | ResNet34 |
| Encoder Weights | ImageNet |
| Framework | PyTorch |
| Input Size | 512 × 512 |
| Output | Binary Segmentation Mask |

---

# 🎯 Loss Function

The model uses a combined loss:

- Binary Cross Entropy (BCE)
- Dice Loss

This combination helps improve segmentation quality while handling class imbalance effectively.

---

# 📈 Evaluation Metrics

Model performance is evaluated using:

- Dice Score
- Intersection over Union (IoU)
- Validation Loss
- Training Loss

---

# ⚙️ Training Configuration

| Parameter | Value |
|-----------|-------|
| Optimizer | AdamW |
| Learning Rate | 1e-4 |
| Scheduler | ReduceLROnPlateau |
| Epochs | 30 |
| Early Stopping | Yes |
| Batch Loading | PyTorch DataLoader |

---

# 📊 Visualizations

The notebook provides visualizations for:

- Original Images
- Ground Truth Masks
- Predicted Masks
- Dataset Samples
- Training Loss Curves
- Validation Curves
- IoU Progress
- Dice Score Progress

---

# 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/RoadLane-Segmentation.git
```

Move into the project folder:

```bash
cd RoadLane-Segmentation
```

Install dependencies:

```bash
pip install torch torchvision
pip install segmentation-models-pytorch
pip install albumentations
pip install opencv-python
pip install matplotlib
pip install numpy
pip install scikit-learn
pip install kagglehub
pip install tqdm
```

---

# ▶️ Run the Notebook

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```
RoadLane_Segmentation.ipynb
```

Run all cells to:

- Download the dataset
- Prepare the data
- Train the model
- Evaluate performance
- Visualize predictions

---

# 🎯 Learning Outcomes

This project demonstrates:

- Semantic Segmentation
- U-Net Architecture
- Transfer Learning
- Image Preprocessing
- Data Augmentation
- Deep Learning Model Training
- Model Evaluation
- PyTorch Dataset Design
- Binary Image Segmentation

---

# 💡 Future Improvements

- DeepLabV3+
- U-Net++
- Attention U-Net
- EfficientNet Encoder
- Mixed Precision Training
- ONNX/TorchScript Export
- Real-time Video Lane Segmentation
- Model Deployment using FastAPI
- TensorRT Optimization
- Multi-Class Road Scene Segmentation

---

# 👨‍💻 Author

**Muhammad Hassan Tahir**

AI Engineer | Machine Learning | Computer Vision | Deep Learning

---

# 📜 License

This project is intended for educational and research purposes.
