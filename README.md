# Edge AI & AI-IoT Assignment — README

## 📌 Project Overview
This repository contains the full implementation and documentation for the **Emerging AI Trends Assignment**, covering:
- **Edge AI Prototype** (TensorFlow Lite image classifier)
- **AI + IoT Smart Agriculture System Design**
- **Theoretical analysis of Edge AI and Quantum AI**

This README gives setup instructions, file descriptions, dataset guidance, and deployment steps.

---

## 📂 Repository Structure
```
/assignment-edge-ai/
|-- edge_ai_recyclables.ipynb        # Jupyter/Colab notebook for training & TFLite conversion
|-- recycle_mobilenetv2.tflite       # Exported TFLite model (if included)
|-- labels.txt                       # Class labels for inference
|-- inference_pi.py                  # Raspberry Pi real-time inference script
|-- system_design.md                 # AI-IoT concept description + diagram
|-- diagrams/                        # Mermaid diagrams or PNG exports
|-- reports/                         # Accuracy plots, confusion matrix
|-- README.md                        # This file
```

---

## 🧠 Part 1 — Theory Summary
### **Edge AI Advantages**
- Reduces latency by running inference on-device
- Protects privacy by processing sensitive data locally
- Useful in autonomous drones, robotics, and smart cameras

### **Quantum AI vs Classical AI**
- Quantum AI excels in combinatorial optimization via QAOA/annealing
- Beneficial for logistics, finance, telecoms, chemistry

(Full detailed answers in main report or canvas document.)

---

## 🛠 Part 2 — Edge AI Prototype
### **1. Dataset Preparation**
Use any recyclables dataset from **Kaggle**.
Upload and arrange it like this:
```
/data/train/<class_name>/images...
/data/val/<class_name>/images...
```
Examples of classes:
- plastic
- glass
- metal
- paper

### **2. Notebook Instructions (edge_ai_recyclables.ipynb)**
The notebook includes:
- Data loading
- MobileNetV2 transfer learning
- Training & evaluation
- TFLite conversion with quantization
- Inference validation using the TFLite interpreter

Run all cells in order on **Google Colab**.

### **3. Model Output**
Running the notebook generates:
- `recycle_mobilenetv2.tflite`
- `labels.txt`

These are needed for real-time edge inference.

---

## 🍓 Raspberry Pi Deployment
### **Requirements**
- Raspberry Pi 3/4 (recommended)
- Camera module or USB webcam
- Python 3.8+

### **Install dependencies**
```bash
sudo apt update
pip install tflite-runtime opencv-python-headless numpy
```

### **Run inference**
```bash
python3 inference_pi.py
```

The script prints real-time classification results for recyclables.

---

## 🌾 AI-IoT Smart Agriculture Concept
Full design documented in `system_design.md`.
Includes:
- Sensor list (soil moisture, temp, pH, EC, light)
- Data flow architecture (edge → cloud → dashboard)
- ML model proposal (LSTM/GRU or XGBoost)
- Mermaid diagram

---

## 📊 Evaluation Metrics
### Edge AI Model
- Accuracy, loss curves
- Confusion matrix
- Latency on Raspberry Pi

### AI-IoT System
- RMSE / MAE for crop yield regression
- Water-saving percentage

---

## 🧪 How to Reproduce
### **Step 1: Clone repo**
```bash
git clone <AI-for-SE-wk-6>
cd assignment-edge-ai
```

### **Step 2: Open notebook**
Upload `edge_ai_recyclables.ipynb` to Colab or local Jupyter.

### **Step 3: Run all cells**
Generate the TFLite model.

### **Step 4: Deploy**
Copy `.tflite` and `labels.txt` to a Raspberry Pi.

---

## 📝 Notes
- This project is designed to simulate Edge AI without requiring physical hardware.
- If you don't have a Pi, use Colab's TFLite Interpreter testing section.
- Sensors in AI-IoT design are conceptual unless implemented with real hardware.

---

## ✔ Submission Checklist
- [ ] Notebook complete (training + TFLite)
- [ ] Accuracy plots added to `reports/`
- [ ] README updated with dataset link
- [ ] AI-IoT design in `system_design.md`
- [ ] Code pushed to GitHub

---

