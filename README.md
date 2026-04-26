&lt;div align="center"&gt;

&lt;img src="New-Logo.png" alt="Googles Detection Model Logo" width="220"/&gt;

&lt;h1&gt;🔍 Safety Goggles Detection Model&lt;/h1&gt;

&lt;p&gt;&lt;strong&gt;AI-Powered Computer Vision for Workplace Safety Compliance&lt;/strong&gt;&lt;/p&gt;

&lt;p&gt;
  &lt;img src="https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white"/&gt;
  &lt;img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white"/&gt;
  &lt;img src="https://img.shields.io/badge/YOLO-v8-00FFFF?style=for-the-badge&logo=yolo&logoColor=black"/&gt;
  &lt;img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white"/&gt;
&lt;/p&gt;

&lt;p&gt;
  &lt;img src="https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square"/&gt;
  &lt;img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/&gt;
&lt;/p&gt;

&lt;/div&gt;

---

## 🎯 About

A **Deep Learning & Computer Vision model** built with **YOLO** and **PyTorch** to detect whether workers are wearing safety goggles — preventing eye injuries and ensuring workplace safety compliance.

**Target environments:** Manufacturing plants, construction sites, laboratories, and industrial facilities.

---

## ✨ Features

- 🎥 **Real-Time Detection** — Live video stream analysis
- 👤 **Multi-Person Tracking** — Detect multiple workers at once
- 🟢🔴 **Compliance Scoring** — Instant visual feedback (Green = Compliant, Red = Violation)
- 📊 **Custom Dataset** — Entire dataset created from scratch by the author
- 🚀 **Fast Inference** — Optimized for real-world deployment

---

## 🛠 Tech Stack

| Technology | Purpose |
|------------|---------|
| **YOLO** | Object detection backbone |
| **PyTorch** | Deep learning framework |
| **OpenCV** | Image/video processing |
| **NumPy / Pandas** | Data manipulation |

---

## ⚙️ Quick Start

```bash
# Clone repo
git clone https://github.com/omardiab9951/Googles-Detection-Model.git
cd Googles-Detection-Model

# Setup environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run detection
python detect.py --source 0 --weights best.pt

📊 Dataset
The entire dataset was created from scratch by me, featuring:
Various lighting conditions (indoor, outdoor, low-light)
Different goggle types (clear, tinted, prescription)
Multiple face orientations and ethnicities
Real-world industrial backgrounds


