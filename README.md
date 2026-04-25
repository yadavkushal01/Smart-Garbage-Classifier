# 🗑️ Smart Garbage Classifier — AI Waste Classification System

> An end-to-end deep learning web application that classifies waste images into 6 categories in real time, built during my Machine Learning Internship at **Edunet Foundation**.

---

## 📌 Overview

Improper waste disposal is a major environmental challenge. This project addresses it by building an AI-powered garbage classification system that can identify the type of waste from an uploaded image and suggest appropriate disposal methods — all through a simple web interface.

**Achieved 84% classification accuracy** across 6 waste categories using transfer learning.

---

## 🎯 Features

- 📸 Upload any waste image and get instant classification
- 🧠 Deep learning model using **MobileNetV2 transfer learning**
- 📊 Displays prediction confidence scores for all categories
- 🌐 Clean, interactive web UI built with **Streamlit**
- ⚡ Real-time inference with no manual setup required

---

## 🗂️ Waste Categories

| Category | Description |
|----------|-------------|
| 🥤 Plastic | Bottles, bags, containers |
| 🍾 Glass | Bottles, jars, broken glass |
| 🥫 Metal | Cans, foil, scrap metal |
| 📰 Paper | Newspapers, cardboard, boxes |
| 📦 Cardboard | Corrugated boxes, packaging |
| 🗑️ Trash | General non-recyclable waste |

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Language | Python 3.x |
| Deep Learning | TensorFlow, Keras |
| Model Architecture | CNN + MobileNetV2 (Transfer Learning) |
| Web App | Streamlit |
| Data Processing | NumPy, Pandas |
| Dataset | Kaggle Garbage Classification Dataset |

---

## 🧠 Model Architecture

```
Input Image (224x224x3)
        ↓
MobileNetV2 (Pre-trained on ImageNet) — Feature Extraction
        ↓
Global Average Pooling
        ↓
Dense Layer (128 units, ReLU)
        ↓
Dropout (0.3)
        ↓
Output Layer (6 units, Softmax) — Classification
```

**Training details:**
- Transfer learning with frozen MobileNetV2 base layers
- Data augmentation: rotation, flipping, zoom, brightness adjustment
- Optimizer: Adam | Loss: Categorical Crossentropy
- Final Accuracy: **84%** on validation set

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/yadavkushal01/Edunet-Project.git
cd Edunet-Project

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the Streamlit app
streamlit run app1.py
```

Then open `http://localhost:8501` in your browser, upload a waste image, and get instant classification results!

---

## 📁 Project Structure

```
Edunet-Project/
│
├── app1.py                  # Main Streamlit web app
├── project.py               # Model training script
├── fix_labels.py            # Dataset label preprocessing
├── garbage_classifier.h5    # Trained model weights
├── requirements.txt         # Python dependencies
└── dataset/                 # Training data directory
```

---

## 📈 Results

- **Validation Accuracy:** 84%
- **Classes:** 6 waste categories
- **Training Images:** ~2,500 images (post augmentation)
- **Model Size:** ~15MB (MobileNetV2 optimized)

---

## 🔮 Future Improvements

- [ ] Improve accuracy to 90%+ with fine-tuning
- [ ] Add mobile-responsive design
- [ ] Deploy on cloud (Heroku / Render)
- [ ] Add disposal recommendation for each waste type

---

## 👨‍💻 Author

**Kushal Yadav** — ML Intern @ Edunet Foundation  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/kushal-yadav-067ab4334)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](https://github.com/yadavkushal01)

---

> ⭐ If you found this project useful, please consider giving it a star!
