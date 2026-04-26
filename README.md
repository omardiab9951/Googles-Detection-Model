<div align="center">

<img src="https://img.shields.io/badge/Safety%20AI-Industrial%20Vision-FF4500?style=for-the-badge" />
<img src="https://img.shields.io/badge/Model-YOLOv8-00C4CC?style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/Task-Object%20Detection-blueviolet?style=for-the-badge" />
<img src="https://img.shields.io/badge/Domain-Computer%20Vision-228B22?style=for-the-badge" />

# 🥽 Goggles Detection Model
### Real-Time Safety Goggles Compliance Detection for Industrial Environments

*A production-ready deep learning pipeline that detects whether workers are wearing safety goggles — preventing accidents before they happen.*

[![Author](https://img.shields.io/badge/Author-Omar%20Diab-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/omar9951)
[![GitHub](https://img.shields.io/badge/GitHub-omardiab9951-181717?style=flat-square&logo=github)](https://github.com/omardiab9951)

</div>

---

## 🔍 Overview

In high-risk industrial environments — factories, laboratories, construction sites, and chemical plants — failing to wear safety goggles is one of the most common causes of severe eye injuries and costly insurance claims. Manual monitoring is impractical at scale.

This project delivers a **real-time computer vision system** that automatically detects whether workers are wearing safety goggles using a fine-tuned **YOLOv8** object detection model. Designed to integrate with existing CCTV infrastructure, it provides instant compliance monitoring without human oversight.

### 💡 The Problem
- Eye injuries account for a significant share of workplace accidents globally
- Manual PPE inspections are inconsistent, labor-intensive, and reactive rather than preventive
- Non-compliance drives up medical insurance costs for employers and endangers lives

### ✅ The Solution
An always-on, camera-based AI system that:
- Detects **goggles** vs **no goggles** in real time
- Flags non-compliant workers instantly for supervisor alerts
- Creates an auditable compliance log — automating what used to require human eyes

---

## 🏗️ Model Architecture

| Component | Details |
|---|---|
| **Base Architecture** | YOLOv8m (medium variant) |
| **Task** | Object Detection (2-class) |
| **Classes** | `goggles` · `no_goggle` |
| **Optimizer** | AdamW with cosine learning rate scheduling |
| **Augmentation** | Mosaic, HSV shifts, random flip, scale jitter, copy-paste |
| **Input Resolution** | 640 × 640 |
| **Training Platform** | Kaggle (Tesla T4 GPU) |

The model was developed across multiple training iterations (v1–v4), scaling from YOLOv8n/s up to YOLOv8m with progressively refined hyperparameters and augmentation strategies, informed by rigorous per-class diagnostic analysis at each stage.

---

## 📦 Dataset

- **Collection:** Manually collected by the author — images sourced and curated specifically for goggles detection in industrial contexts
- **Labeling:** Annotated and labeled using **Roboflow**, with bounding boxes drawn exclusively around goggles regions
- **Classes:** 2 — `goggles` (compliant), `no_goggle` (non-compliant)
- **Format:** YOLO-format bounding box annotations
- **Split:** Train / validation split configured via Roboflow's export pipeline

> ⚠️ The dataset exhibits natural class imbalance — goggles instances are more frequent than no_goggle instances. Augmentation strategies and loss weighting were carefully applied to mitigate this.

---

## 🛠️ Installation & Usage

### Prerequisites
```bash
pip install ultralytics
pip install opencv-python
```

### Clone the Repository
```bash
git clone https://github.com/omardiab9951/Googles-Detection-Model.git
cd Googles-Detection-Model
```

### Run Inference on an Image
```python
from ultralytics import YOLO

model = YOLO("weights/best.pt")
results = model.predict(source="your_image.jpg", conf=0.5, save=True)
results[0].show()
```

### Run Real-Time Webcam Detection
```python
from ultralytics import YOLO

model = YOLO("weights/best.pt")
model.predict(source=0, conf=0.5, show=True)  # source=0 for webcam
```

### Run on Video File
```python
from ultralytics import YOLO

model = YOLO("weights/best.pt")
model.predict(source="factory_footage.mp4", conf=0.5, save=True)
```

---

## 🎯 Target Use Cases

| Environment | Application |
|---|---|
| 🏭 Manufacturing Plants | Assembly line worker compliance monitoring |
| 🔬 Laboratories | Chemical handling safety enforcement |
| 🏗️ Construction Sites | Real-time PPE audit via site cameras |
| ⚡ Electrical Utilities | High-voltage area access control |
| 🏥 Medical Facilities | Sterile zone compliance verification |

---

## 📈 Why This Matters

> The International Labour Organization estimates that **2.3 million workers** die annually from work-related accidents and diseases. Eye injuries alone cost employers billions in medical insurance, legal liability, and lost productivity every year.

A passive, always-on AI compliance layer represents a paradigm shift: from **reactive incident response** to **proactive prevention** — at a fraction of the cost of dedicated safety personnel.

---

## 🔭 Roadmap & Future Work

- [ ] Expand to full PPE detection suite: helmets, gloves, high-vis vests, face masks
- [ ] Edge deployment: ONNX / TensorRT export for NVIDIA Jetson and Raspberry Pi
- [ ] Multi-camera scene tracking with worker ID association across frames
- [ ] Live alert system integration (Slack, SMS, monitoring dashboard)

---

## 👤 Author

**Omar Diab**
Data Science & AI Student — ElSewedy University of Technology, Polytechnic of Egypt

[![LinkedIn](https://img.shields.io/badge/LinkedIn-omar9951-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/omar9951)
[![GitHub](https://img.shields.io/badge/GitHub-omardiab9951-181717?style=flat-square&logo=github)](https://github.com/omardiab9951)
[![Email](https://img.shields.io/badge/Email-omarkamaldiab9951@gmail.com-EA4335?style=flat-square&logo=gmail)](mailto:omarkamaldiab9951@gmail.com)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

<div align="center">

*Built with purpose — because the best safety system is the one that never sleeps.*

⭐ If this project helped you, consider giving it a star!

</div>
