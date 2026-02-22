# 🧠 MultimodalAI_for_AlzheimerPrediction

A Full-Stack Multimodal Explainable AI Web Application for Alzheimer’s Disease Risk Prediction using:

- 📊 Clinical / Tabular Data  
- 🧠 MRI Brain Imaging  
- 🎤 Speech Audio Signals  
- 🔍 SHAP Explainability  
- 🔥 Grad-CAM Visualization  
- 🌐 Flask Web Deployment  

---

## 🚀 Project Overview

**MultimodalAI_for_AlzheimerPrediction** is an end-to-end AI-powered web platform that predicts Alzheimer’s disease risk by integrating three independent diagnostic modalities into a unified decision framework.

Unlike traditional single-input systems, this platform:

- Uses independent deep learning models for each modality  
- Performs weighted multimodal fusion  
- Generates interpretable explanations using SHAP  
- Visualizes MRI attention regions using Grad-CAM  
- Provides clinician-friendly recommendations  
- Stores patient history securely using SQLite  

---

# 🖼️ Application Screenshots

---

## 📊 Clinical Data Upload (Tabular Input)

<img width="1902" height="1020" alt="image" src="https://github.com/user-attachments/assets/01646fa5-7af5-463b-9cb8-cb5b9956b4c2" />

<img width="1902" height="1065" alt="image" src="https://github.com/user-attachments/assets/3b44c0e3-d7d9-41ff-abba-d201892a3413" />

Users enter cognitive scores, demographics, and clinical indicators which are processed using a Random Forest classifier.

---

## 🧠 MRI Image Upload

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/64297568-c99d-4382-9aa0-ad0e5691aee8" />



Users upload MRI brain scans. The VGG16 CNN model processes the image and predicts the disease stage.

---

## 🎤 Audio Upload

<img width="1293" height="671" alt="image" src="https://github.com/user-attachments/assets/f6d0b129-d903-425c-9506-5c8b3afc9b89" />

Users upload speech recordings. MFCC features are extracted and fed into the ConvLSTM model.

---

## 📈 Final Result Page

<img width="1293" height="671" alt="image" src="https://github.com/user-attachments/assets/1c2cbfae-7e58-4c27-8499-2246e092d388" />



The system displays:

- Individual model predictions  
- Fusion risk score  
- Final Alzheimer risk classification  
- Clinical recommendations  

---

# 🔍 Explainability Outputs

<img width="1413" height="680" alt="image" src="https://github.com/user-attachments/assets/22958c15-e97a-4e1d-84c0-485b228d9a2e" />

![Uploading image.png…]()

The system provides multimodal interpretability using SHAP and Grad-CAM, consolidated into a single comprehensive visualization.

This combined explainability output includes:

### 📊 Clinical SHAP
- Feature importance summary for tabular inputs  
- Identifies the most influential cognitive and demographic variables  

### 🧠 MRI SHAP + Grad-CAM
- Pixel-level SHAP visualization  
- Grad-CAM heatmap overlay  
- Highlights brain regions influencing Alzheimer prediction  

### 🎤 Audio SHAP
- MFCC importance heatmap  
- Shows acoustic features contributing to classification  

These explainability techniques enhance clinical transparency and help interpret how each modality contributes to the final Alzheimer risk prediction.


# 🏗️ System Architecture

### 🔹 Multimodal Pipeline

Clinical Input → Random Forest  
MRI Image → VGG16 CNN  
Audio Signal → ConvLSTM Model  

↓  
Weighted Fusion Layer  
↓  
Risk Score Computation  
↓  
Final Alzheimer Risk Classification  
↓  
Explainability (SHAP + Grad-CAM)  
↓  
Clinical Recommendations  

---

# 🧠 Models Used

## 1️⃣ Clinical Model

- Algorithm: Random Forest  
- Explainability: SHAP TreeExplainer  

## 2️⃣ MRI Image Model

- Architecture: VGG16 (Fine-Tuned)  
- Explainability: SHAP + Grad-CAM  

## 3️⃣ Audio Model

- Architecture: ConvLSTM  
- Feature Extraction: MFCC  
- Explainability: SHAP KernelExplainer  

---

# 🧪 Multimodal Fusion Strategy

Text Model → 30%  
MRI Model → 40%  
Audio Model → 30%  

Fusion Formula:

fusion_score =  
0.3 × Text_Risk × Text_Confidence +  
0.4 × Image_Risk × Image_Confidence +  
0.3 × Audio_Risk × Audio_Confidence  

Final Output:

- High Alzheimer Risk  
- Low / No Alzheimer Risk  

---

# 🌐 Web Application Features

## 🔐 Authentication
- User Registration  
- Admin Approval  
- Role-Based Access  

## 📊 Dashboard
- Total Predictions  
- Risk Distribution  

## 📁 History
- View past predictions  
- Track fusion scores  

---

# ⚙️ Installation

Clone repository:

```
git clone https://github.com/yourusername/MultimodalAI_for_AlzheimerPrediction.git
cd MultimodalAI_for_AlzheimerPrediction
```

Install dependencies:

```
pip install -r requirements.txt
```

Run application:

```
python app.py
```

Open:

```
http://127.0.0.1:5000
```

---

# 📦 Requirements

- Python 3.9+  
- Flask  
- TensorFlow / Keras  
- Scikit-learn  
- SHAP  
- Librosa  
- NumPy  
- Pandas  
- Matplotlib  
- SQLite3  

---

# ⚠️ Important

This project is for research and educational purposes only and is not intended for clinical diagnosis.

---

# 📜 License

MIT License

