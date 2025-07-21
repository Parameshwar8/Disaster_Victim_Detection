# 🛑 Disaster Victim Detection using YOLOv5 and Deep Learning

This project aims to assist in post-disaster response by automatically detecting victims in images using advanced deep learning techniques. The system combines YOLOv5 for real-time object detection and ResNet50 for feature extraction, followed by classical machine learning classifiers for enhanced accuracy.

---

## 📌 Features

- 🔍 **Human Detection using YOLOv5**
- 🧠 **ResNet50-based Feature Extraction**
- 🤖 Classification using:
  - Decision Tree
  - Support Vector Machine (SVM)
  - Random Forest
- 🖥️ **Tkinter GUI** to upload and classify images
- 📊 Model evaluation and accuracy comparison
- 🖼️ Support for synthetic and real aerial imagery

---

## 🧠 Methodology

1. **YOLOv5 Detection**:
   - Load YOLOv5 pretrained model to detect people in input images
   - Crop detected regions for further classification

2. **Image Preprocessing**:
   - Resize cropped regions to 224x224
   - Normalize pixel values and convert to numpy arrays

3. **Feature Extraction**:
   - Use pretrained ResNet50 (without top layers) to extract high-level features

4. **Classification**:
   - Train SVM, Decision Tree, and Random Forest classifiers on extracted features
   - Predict whether the detected person is a **victim** or **non-victim**

5. **GUI Interface**:
   - Upload image
   - Run YOLOv5 detection
   - Choose a classifier and get victim classification

---

## 🖼️ GUI Preview

> *(Insert screenshot here if available)*

Features:
- Upload image
- Run detection using YOLOv5
- Choose classifier for victim status prediction
- Display bounding boxes and prediction results

---

## 📁 Project Structure

```
Disaster_Victim_Detection/
├── yolov5/                        # YOLOv5 cloned repo or model weights
├── Disaster_Victim_Detection.ipynb # Full pipeline Jupyter Notebook
├── gui.py                         # Tkinter GUI with YOLOv5 + classifier integration
├── models/                        # Trained classifiers (SVM, RF, etc.)
├── images/                        # Sample and test images
├── requirements.txt               # Python dependencies
└── README.md                      # Project documentation
```

---

## ⚙️ Requirements

Install dependencies:

```bash
pip install -r requirements.txt
```

Additional steps:
- Clone YOLOv5 repo (if not already):
```bash
git clone https://github.com/ultralytics/yolov5
cd yolov5
pip install -r requirements.txt
```

---

## ▶️ How to Run

1. Clone the repository:

```bash
git clone https://github.com/your-username/Disaster_Victim_Detection.git
cd Disaster_Victim_Detection
```

2. Run the GUI:

```bash
python gui.py
```

3. In the GUI:
   - Upload image
   - Click “Detect Victims” to run YOLOv5
   - Choose classifier and classify detected people

---

## 📊 Sample Output

```
Detected: 3 persons

Person 1: Victim [SVM, 91.2% confidence]
Person 2: Non-Victim [RF, 87.3% confidence]
Person 3: Victim [Decision Tree, 89.1% confidence]
```

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 🙋‍♂️ Acknowledgments

This project was developed for disaster response automation using deep learning and computer vision.

**Developed by: Parameshwar V.**
