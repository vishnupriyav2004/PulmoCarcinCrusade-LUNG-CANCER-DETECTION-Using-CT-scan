# PulmoCarcinCrusade-LUNG-CANCER-DETECTION-Using-CT-scan
PulmoCarcinCrusade is an AI-powered diagnostic system that automates the detection and stage classification of lung cancer using CT scan images. It combines traditional machine learning (SVM, Ensemble) with deep learning (CNN) to classify cases as Normal, Benign, or Malignant, and further identifies the cancer stage (I–IV) in abnormal cases.

📘 Overview
PulmoCarcinCrusade is a computer-aided diagnosis (CAD) system that empowers early detection and staging of lung cancer using CT scan images and artificial intelligence. It classifies lung conditions into Normal, Benign, or Malignant, and further stages cancer cases into Stage I to IV using image-based texture analysis.

🧠 Technologies & Models Used
Dataset: IQ-OTH/NCCD (CT scans from Iraq Oncology Teaching Hospital)

**Machine Learning:**

  Support Vector Machine (SVM) with handcrafted Gabor + GLCM features
  
  Ensemble Model: SVM + Random Forest + Gradient Boosting (Soft Voting)

**Deep Learning:**

  Convolutional Neural Network (CNN) for automatic feature extraction and classification
  
  Staging: Texture-based GLCM analysis for Stage I–IV detection in abnormal cases

**Preprocessing:**

  Bit-plane slicing
  Gaussian filtering
  Erosion
  SMOTE (Synthetic Minority Over-sampling Technique)
  PCA (Principal Component Analysis)

**🧪 Features**
  ✅ Lung cancer classification: Normal, Benign, Malignant
  
  🔬 Stage-wise classification: Stage 1 to Stage 4 (for abnormal cases)
  
  🎯 Multiple model comparison: SVM vs Ensemble vs CNN
  
  📈 Evaluation Metrics: Accuracy, Precision, Recall, F1-Score
  
  📊 CNN achieved 100% accuracy on test data
  

🏗️ **Project Architecture**
  🔹 ML/Ensemble Model
    Image preprocessing → Feature extraction (GLCM + Gabor) → PCA → SMOTE → Classification using SVM, RF, GB
    
  🔹 CNN Model
    Preprocessed CT images → CNN training → Classification → GLCM-based staging

Model      	Accuracy	Precision	Recall	F1-Score
SVM	        ~89.9%	    0.88      	0.87	0.87
Ensemble	     ~94%      0.93	      0.93	0.93
CNN	           100%     1.00	      1.00	1.00
