🧠 MultimodalAI_for_AlzheimerPrediction

A Full-Stack Multimodal Explainable AI Web Application for Alzheimer’s Disease Risk Prediction using:

📊 Clinical / Tabular Data

🧠 MRI Brain Imaging

🎤 Speech Audio Signals

🔍 SHAP Explainability

🔥 Grad-CAM Visualization

🌐 Flask Web Deployment

🚀 Project Overview

MultimodalAI_for_AlzheimerPrediction is an end-to-end AI-powered web platform that predicts Alzheimer’s disease risk by integrating three independent diagnostic modalities into a unified decision framework.

Unlike traditional single-input systems, this platform:

Uses independent deep learning models for each modality

Performs weighted multimodal fusion

Generates interpretable explanations using SHAP

Visualizes MRI attention regions using Grad-CAM

Provides clinician-friendly recommendations

Stores patient history securely using SQLite

This system is designed for research demonstration and academic deployment in clinical AI environments.

🏗️ System Architecture
🔹 Multimodal Pipeline

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

🧠 Models Used
1️⃣ Clinical Model (Tabular Data)

Algorithm: Random Forest

Preprocessing: StandardScaler

Output: Presence / Absence

Explainability: SHAP TreeExplainer

Captures:

Cognitive test scores

Demographic patterns

Risk factors

2️⃣ MRI Image Model

Architecture: VGG16 (Fine-Tuned)

Input Size: 224 × 224

Output Classes:

AD

CN

EMCI

LMCI

MCI

Explainability:

SHAP DeepExplainer

Grad-CAM heatmap visualization

Grad-CAM highlights:

Hippocampal atrophy

Temporal lobe degeneration

Structural abnormalities

3️⃣ Audio Model

Architecture: ConvLSTM

Feature Extraction: MFCC (40 coefficients)

Output:

Alzheimer

Healthy

Explainability:

SHAP KernelExplainer

MFCC importance heatmap

Captures:

Tremor

Pitch instability

Voice degradation patterns

🧪 Multimodal Fusion Strategy

Weighted Risk Fusion:

Text Model → 30%
MRI Model → 40%
Audio Model → 30%

Fusion Formula:

fusion_score =
0.3 × Text_Risk × Text_Confidence +
0.4 × Image_Risk × Image_Confidence +
0.3 × Audio_Risk × Audio_Confidence

Final Classification:

High Alzheimer Risk (score ≥ 0.5)

Low / No Alzheimer Risk (score < 0.5)

🔍 Explainability Framework
SHAP Explanations

The system generates three SHAP explanations:

📊 Clinical SHAP

Feature importance summary plot

Shows most influential tabular variables

🧠 MRI SHAP

Pixel-level explanation

Highlights brain regions contributing to prediction

🎤 Audio SHAP

MFCC importance heatmap

Shows acoustic features affecting classification

🔥 Grad-CAM (For MRI)

Grad-CAM is integrated for CNN interpretability.

It:

Computes gradients of target class

Produces heatmap overlay on MRI image

Highlights regions influencing AD prediction

This provides visual transparency for clinicians.

🌐 Web Application Features
🔐 Authentication System

User Registration

Admin Approval Required

Secure Login

Role-Based Access (Admin / User)

Admin Account (default):
admin@gmail.com

Password: admin

📊 User Dashboard

Displays:

Total predictions

High-risk cases

Low-risk cases

🧾 Patient Workflow

Enter Clinical Data

Upload MRI Image

Upload Audio File

View Results

View SHAP & Grad-CAM Explanations

Get Recommendations

Save to History

📁 History Module

Users can:

View past predictions

Track patient risk progression

View stored fusion scores

🗂️ Project Structure
MultimodalAI_for_AlzheimerPrediction/
│
├── models/
│   ├── rf_model.pkl
│   ├── scaler.pkl
│   ├── feature_order.pkl
│   ├── vgg16_adni_final2.h5
│   └── Alzheimer_Audio_ConvLSTM_SHAP.h5
│
├── static/
│   ├── uploads/
│   ├── shap_plots/
│
├── templates/
│   ├── login.html
│   ├── register.html
│   ├── dashboard.html
│   ├── admin.html
│   ├── input.html
│   ├── image_input.html
│   ├── audio_input.html
│   ├── output.html
│   ├── history.html
│
├── users.db
├── app.py
├── requirements.txt
└── README.md
⚙️ Installation
1️⃣ Clone Repository
git clone https://github.com/yourusername/MultimodalAI_for_AlzheimerPrediction.git
cd MultimodalAI_for_AlzheimerPrediction
2️⃣ Install Dependencies
pip install -r requirements.txt
3️⃣ Run Application
python app.py

Open browser:

http://127.0.0.1:5000

📦 Requirements

Python 3.9+

Core Libraries:

Flask

TensorFlow / Keras

Scikit-learn

SHAP

Librosa

NumPy

Pandas

Matplotlib

SQLite3

📊 Database Schema
Users Table

id

username

password

is_admin

is_approved

Results Table

patient_id

username

text_label

image_label

audio_label

fusion_label

fusion_score

date

🏥 Clinical Recommendation Engine

Based on model outputs, the system provides suggestions such as:

Neurologist consultation

MRI follow-up

Speech therapy

Cognitive lifestyle monitoring

🎯 Key Contributions

✔ Multimodal Deep Learning Integration
✔ Full Flask Deployment
✔ SHAP Explainability (3 modalities)
✔ Grad-CAM Visualization
✔ Admin-Controlled Medical Dashboard
✔ Weighted Risk Fusion Strategy

🔬 Research Impact

This system demonstrates:

Practical multimodal AI integration

Clinically interpretable deep learning

Explainable AI in healthcare

Full-stack medical AI deployment

It bridges research models with real-world web implementation.

🚀 Future Enhancements

3D CNN for volumetric MRI

Transformer-based multimodal fusion

Docker containerization

JWT-based authentication

REST API version

Real-time voice recording

Cloud deployment (AWS / Azure)


Important

This project is for research and educational purposes only and is not intended for clinical diagnosis.
