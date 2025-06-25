# 🛌 Sleep Apnea Detection using Multi-Modal Deep Learning (Colab)

This project is a deep learning-based system for detecting **sleep apnea** using data collected from wearable devices. The models are implemented and executed in a single **Google Colab notebook**, making it easy to test and demonstrate without local setup.

---

## 🧠 What It Does

The system uses **two separate models**:

### 1. Audio-based Snoring Detection
- Input: Audio recordings during sleep (converted to MFCCs/spectrograms)
- Model: LSTM-CNN
- Output: Probability of snoring event

### 2. HRV & SpO₂-based Apnea Detection
- Input: Heart Rate Variability (HRV) and Blood Oxygen Saturation (SpO₂) data
- Model: LSTM
- Output: Probability of apnea event

---

## 🔗 Fusion Logic

The predictions from both models are combined using **weighted averaging**:
Final Score = 0.4 × Snoring Score + 0.6 × HRV/SpO₂ Score


### Based on the Final Score:
- **0.0 – 0.3** → No Vibration
- **0.3 – 0.5** → Mild Vibration
- **0.5 – 0.7** → Moderate Vibration
- **> 0.7** → Strong Vibration

This vibration feedback can be integrated with a **smartwatch or wearable device** to alert the user and prevent prolonged apneic episodes.

---

## ✅ Project Highlights

- Fully implemented in **Google Colab** — no setup required
- Focused on **real-time detection** using wearable-compatible data
- Modular and easily extendable for medical research

---

## 📁 Contents

- `Sleep_Apnea_Detection.ipynb`: Main Colab notebook containing:
  - Data preprocessing
  - Model training
  - Prediction fusion
  - Vibration logic

---

## 👨‍💻 Author

**Yashovardhan Harit**  
VIT Chennai  
Email: *yashovardhan.harit2022@vitstudent.ac.in*

**Kanishk Sharma**  
VIT Chennai  
Email: *kanishk.sharma2022a@vitstudent.ac.in*

---

## 📜 License

This project is for academic and research use. Feel free to fork and extend with credit.