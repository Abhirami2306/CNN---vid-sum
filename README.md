📽️ Video Summarization using CNN, Autoencoder & Random Forest
A deep learning-powered system that intelligently condenses videos by identifying and extracting the most important frames. This technique helps reduce video length while preserving critical content, making it useful for surveillance, media, education, and content analysis.

🧠 Overview
This project leverages a combination of:

🧩 Convolutional Neural Networks (CNN) for feature extraction
🔒 Sparse Autoencoder for compressing frame features
🌲 Random Forest Classifier to detect keyframes
🎞️ OpenCV for video processing and summary generation

The pipeline extracts keyframes based on learned patterns from input videos and can generate summary videos or storyboards.

⚙️ Core Components
1. 🎬 Frame Extraction
Extracts 1 frame per second using OpenCV
Ensures temporal consistency in sampled data

2. 🧠 CNN Feature Extraction
Utilizes VGG16 or InceptionV3 pretrained on ImageNet
Captures rich spatial features from each frame

3. 🔄 Sparse Autoencoder
Applies dimensionality reduction on extracted features
Uses L1 regularization to learn sparse latent representations
Prevents overfitting and improves generalization

4. 🌳 Random Forest Classification
Classifies frames as key or non-key
Trained on reduced features to improve speed and performance

5. 📊 Visualization
Grad-CAM heatmaps for visual interpretability
CNN feature activation maps
Frame-wise attention bar plots
Confusion Matrix, Precision, Recall, F1-Score

📈 Sample Performance
Metric	Value
Precision	1.00
Recall	0.75
F1-Score	0.86

Note: Evaluation is based on a sample video. Ground truth labels recommended for production-level testing.

🛠️ Technologies Used
Languages: Python
Libraries: OpenCV, TensorFlow/Keras, Scikit-learn
Visualization: Matplotlib, Seaborn
Modeling: VGG16, InceptionV3, Autoencoder, Random Forest

📌 Applications
Quick preview of long-form videos
Video indexing and retrieval
Summarizing surveillance footage
Educational video abstraction
Content recommendation previews

🚀 How to Run
Clone the repository
Place your video in the project folder
Update video_path in the script
Run the script:
python video_summary.py
View extracted keyframes and the generated summary video

🔭 Future Improvements
✅ Support for multiple summary formats (video, grid, timeline)
✅ Integrate shot-boundary detection
✅ Use LSTM or Transformers for temporal modeling
✅ Deploy as a web app using Streamlit or Flask
✅ Add GUI for uploading and summarizing videos
