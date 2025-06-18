# 🌿 Corn Leaf Disease Detection Using CNN

This project implements a lightweight Convolutional Neural Network (CNN) model to classify corn plant leaf images into four different disease categories. The goal is to achieve high accuracy with a custom-designed, efficient model instead of relying on heavy pre-trained architectures like ResNet or ViT.

## 📁 Dataset Structure

The dataset should be placed in a folder named `dataset/`, organized into subfolders per class like this:
dataset/
├── Class1/
│ ├── image1.jpg
│ ├── image2.jpg
│ └── ...
├── Class2/
│ └── ...
└── Class4/


This project uses TensorFlow’s `ImageDataGenerator` to split the dataset into 80% training and 20% validation.

## 🧠 Model Architecture

The CNN model is built using `tensorflow.keras` and includes:

- 📥 **Input**: 128×128 RGB images  
- 🧱 2 Convolutional layers with ReLU activation  
- 🌀 MaxPooling layers after each convolution  
- 🧠 Dense layer with 128 neurons  
- ❌ Dropout layer (0.3) to prevent overfitting  
- 🎯 Output layer with 4 units (softmax for multiclass classification)

## 🧪 Training and Validation

The model is compiled using:

- **Optimizer**: Adam  
- **Loss Function**: Categorical Crossentropy  
- **Metrics**: Accuracy

Training is conducted over 10 epochs with real-time data augmentation applied (rotation, zoom, flip, etc.).

## 📈 Results

### 🔹 Accuracy Curve
![Accuracy](Plantdiseasedectection/plant_disease_detection/Accuracy.png)

### 🔹 Loss Curve
![Loss](Plantdiseasedectection/plant_disease_detection/Loss.png)


### 📊 Final Validation Accuracy
Validation accuracy : 0.9519


### 📊 Sample Predictions
![Prediction1](Plantdiseasedectection/plant_disease_detection/output1.png)  
![Prediction2](Plantdiseasedectection/plant_disease_detection/output2.png)


## 💡 Key Takeaways

- A simple custom CNN can achieve competitive accuracy for plant disease detection.
- Data augmentation significantly helps in improving generalization.
- This model is suitable for deployment on devices with limited compute power.

## 🔧 Setup Instructions

Clone this repository:
   ```bash
   git clone https://github.com/your-username/corn_plant_disease_detection.git
   cd corn_plant_disease_detection
 ```

Install dependencies:

        pip install tensorflow numpy matplotlib

Run the script:
   python cnn_corn_disease.py

🛠️ Possible Improvements
   Add more training data for robustness

   Experiment with deeper CNNs or pre-trained models

   Deploy with Streamlit or Flask for a web interface

   Include Grad-CAM visualization for interpretability

## ✍️ Author

**Anupama G Bhat**  
Machine Learning Enthusiast | Aspiring Data Scientist  
📍 India 

This project was developed as part of my hands-on learning in deep learning and computer vision. I welcome feedback, suggestions, or collaboration opportunities.
