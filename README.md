<p align="center">
  <img src="images/Black Gradient Technology YouTube Banner.png" alt="Deepfake Detection System Banner" width="100%">
</p>

# Deepfake Detection System – Deep Dect  

[![Paper Publication](https://img.shields.io/badge/Paper-IJIREICE-blue)](https://ijireeice.com/papers/deepfake-detection-system-using-resnet50-based-lightweight-for-static-images-deep-dect/)  

A lightweight deepfake detection system for **static images**, built using **ResNet50** and deployed with a simple **Streamlit interface**.  
This project demonstrates how deep learning can be applied to detect manipulated (fake) images and provides an accessible web-based tool for real-time usage.  

---

## 🔗 Publication  
📄 **Deepfake Detection System Using ResNet50-Based Lightweight for Static Images – Deep Dect**  
Published in *International Journal of Innovative Research in Electrical, Electronics, Instrumentation and Control Engineering (IJIREICE)*  
👉 [Read the Paper](https://ijireeice.com/papers/deepfake-detection-system-using-resnet50-based-lightweight-for-static-images-deep-dect/)  

---

## 📌 Features  
- ✅ **Deep Learning Model** – Uses ResNet50 with transfer learning for binary classification (Real vs. Fake).  
- ✅ **Simple Web Interface** – Built with Streamlit, requires no local setup for end-users.  
- ✅ **Fast Inference** – Provides predictions under 200ms on CPU.  
- ✅ **Deployment Ready** – Hosted on Hugging Face Spaces for public access.  
- ✅ **User Friendly** – Dark mode UI with clear results and confidence score.  

---

## 🛠️ Tech Stack  
- **Backend (Model)**: TensorFlow/Keras (ResNet50, fine-tuned)  
- **Frontend (UI)**: Streamlit  
- **Languages**: Python 3.8+  
- **Deployment**: Hugging Face Spaces  
- **Libraries**: NumPy, Pillow, TensorFlow, Streamlit  

---

## 📂 Dataset  
- Source: [Kaggle – Deepfake and Real Images](https://www.kaggle.com/datasets/manjilkarki/deepfake-and-real-images)  
- Structure:  
  ```
  dataset/
  ├── Train/
  │   ├── Real/
  │   └── Fake/
  ├── Validation/
  │   ├── Real/
  │   └── Fake/
  └── Test/
      ├── Real/
      └── Fake/
  ```  
- Preprocessing: Resized to **256×256**, normalized, with data augmentation (flip, zoom, rotation).  

---

## ⚙️ System Architecture  
1. **Backend (ResNet50)**  
   - Pre-trained ResNet50 (ImageNet)  
   - Custom layers: Global Average Pooling → Dense(1024, ReLU) → Dropout(0.5) → Dense(1, Sigmoid)  

2. **Frontend (Streamlit)**  
   - Image upload (JPG, PNG)  
   - Preprocessing → Prediction → Confidence display  

3. **Deployment (Hugging Face)**  
   - Model + UI packaged with requirements.txt  
   - Publicly accessible app via browser  

---

## 🚀 Installation & Usage  

### 1️⃣ Clone Repository  
```bash
git clone https://github.com/your-username/deepfake-detection-system-deep-dect.git
cd deep-dect
```

### 2️⃣ Install Dependencies  
```bash
pip install -r requirements.txt
```

### 3️⃣ Run Locally  
```bash
streamlit run app.py
```

### 4️⃣ Upload Image  
- Upload a JPG/PNG file  
- The system classifies it as **Real** or **Deepfake** with a confidence score  

---

## 📊 Results  
- **Training Accuracy**: ~61.89%  
- **Validation Accuracy**: ~60.84%  
- **Inference Time**: 120–200 ms per image (CPU)  
- **Model Size**: ~95 MB  

### Observations  
- Works best on **clean, well-lit facial images**  
- Accuracy drops on **compressed or heavily filtered images**  
- Simple, stable, and accessible for real-time demos  

---

## ⚖️ Limitations  
- Moderate accuracy (~61%) – due to limited dataset size and training duration  
- Generalization issues with newer deepfake techniques  
- Sensitive to compressed/filtered inputs  

---

## 🔮 Future Work  
- Fine-tune deeper ResNet50 layers for better accuracy  
- Train on larger, more diverse datasets  
- Extend support for **video & webcam detection**  
- Integrate **explainability tools (Grad-CAM)**  
- Deploy as a **mobile/web app (PWA)**  
- Add **batch upload & multilingual UI**  

---

## 📸 Screenshots  
### Upload Interface  
![UI Example]()  

### Prediction Output  
- **Real Image → Classified as Real**  
- **Fake Image → Classified as Deepfake**  

---

## 📚 References  
- Rössler et al., FaceForensics++ (2019)  
- Li et al., Eye-Blink Detection (2020)  
- Celeb-DF Dataset  
- Facebook AI, DeepFake Detection Challenge Dataset  
- TensorFlow, Keras, Streamlit Official Docs  

---

## 👨‍💻 Contributors  
- **Your Name** – Developer, Researcher  
- Department of CS & D, MUSE  

---

✨ *This project demonstrates how AI can be used to fight misinformation by detecting manipulated media. Contributions and suggestions are welcome!*  
