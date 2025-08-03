# 🎞️ Video Summarization using CNN, Autoencoder & Random Forest

A deep learning-powered system that intelligently condenses videos by identifying and extracting keyframes. This approach preserves essential content while reducing video length—ideal for surveillance, media, education, and content analytics.

---

## 🧠 Overview

This project combines:

- 🧠 **CNN (Convolutional Neural Networks)** – Feature extraction
- 🔒 **Sparse Autoencoder** – Feature compression
- 🌲 **Random Forest** – Keyframe classification
- 🎮 **OpenCV** – Frame extraction and video processing

---

## ⚙️ Core Components

### 1. 🎬 Frame Extraction
- Extracts 1 frame per second using OpenCV
- Maintains temporal uniformity

### 2. 🧠 CNN Feature Extraction
- Uses pretrained **VGG16** or **InceptionV3** (ImageNet)
- Captures spatial features from each frame

### 3. 🔐 Sparse Autoencoder
- Compresses extracted features
- Applies **L1 regularization** for sparse representations

### 4. 🌳 Random Forest Classifier
- Classifies frames as **key** or **non-key**
- Operates on compressed features for speed

### 5. 📊 Visualization
- **Grad-CAM heatmaps** for interpretability
- **Activation maps**, **attention plots**, **confusion matrix**
- **Precision, Recall, F1-Score**

---

## 📈 Sample Results

| Metric     | Value |
|------------|-------|
| Precision  | 1.00  |
| Recall     | 0.75  |
| F1-Score   | 0.86  |

> *Note: Based on a sample video. Use labeled datasets for large-scale evaluations.*

---

## 🛠️ Technologies

- **Languages**: Python  
- **Libraries**: OpenCV, TensorFlow/Keras, Scikit-learn  
- **Visualization**: Matplotlib, Seaborn  
- **Models**: VGG16, InceptionV3, Sparse Autoencoder, Random Forest

---

## 📌 Applications

- Summarize long videos into key moments
- Video indexing and search
- Surveillance footage analysis
- Quick content previews for recommendation engines
- Educational lecture summarization

---

## 🚀 How to Use

1. Clone this repo:
   ```bash
   git clone https://github.com/yourusername/video-summarization.git
   cd video-summarization
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
3. Run summarization script:
   ```bash
   python main.py --video input.mp4
4. Output:
   Keyframes saved to /output/frames/
   
   Summary video available as summary.mp4
   
   Evaluation metrics printed to console
