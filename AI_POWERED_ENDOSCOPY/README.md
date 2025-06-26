# 🧠 AI-Powered Endoscopy Analysis Tool

## 📌 Overview

An intelligent system for analyzing endoscopic videos, designed to classify **Z-line vs Esophagitis** using deep learning and YOLO-based object detection. Built to assist medical professionals with automated, real-time diagnostics.

---

## 🚀 Features

### 🔍 Core Functionality
- 🎞️ **Automated Frame-by-Frame Video Analysis** using TensorFlow
- ⚠️ **Abnormal Frame Detection** via confidence thresholding
- 🧠 **YOLO Object Detection** for abnormal regions
- 📡 **Real-time Processing** with visual alerts
- 📁 **Batch Frame Processing** with frame skipping control

### 🖥️ User Interface
- 🧩 **GUI** built with PyQt5
- 🖼️ **Live Frame Display** with indicators
- ⏳ **Progress Tracking** via progress bars
- 📂 **Automatic Result Saving**
- 🖋️ **2D Model Viewer** for reference images

---

## 🛠️ Technical Requirements

### 📦 Dependencies
```
Python 3.7+
tensorflow>=2.0
opencv-python
numpy
PyQt5
ultralytics
```

### 📁 Required Files
- `zline_vs_esophagitis_model.h5`: TensorFlow model
- `best.pt`: YOLOv8 weights
- `design.jpg/png`: Optional reference model

---

## ⚙️ Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd endoscopy-analysis-tool
```

2. Install the dependencies:
```bash
pip install tensorflow opencv-python numpy PyQt5 ultralytics
```

3. Place required models in the root directory:
   - `zline_vs_esophagitis_model.h5`
   - `best.pt`
   - `design.jpg` or `design.png` (optional)

---

## ▶️ Usage

### 1. Start the App
```bash
python main.py
```

### 2. Workflow Steps

- **Video Selection**: Choose MP4, AVI, MOV, MKV file
- **Output Folder**: Set output & YOLO results folders
- **Settings**:
  - Threshold (%): default = 50
  - Frame Skip: default = 5
  - Display: all or only abnormal
- **Process Video**: Click "Start Processing"
- **Run YOLO**: Click "Run YOLO on Abnormal Frames"
- **Extras**: View 2D model, track stats

---

## 🧱 Architecture

### 🔧 Components

- **VideoProcessor**: Handles threading, frame extraction, TensorFlow inference
- **YoloProcessor**: Runs YOLOv8 on saved abnormal frames
- **MainWindow**: Orchestrates GUI and logic
- **DesignViewer**: Loads & displays model images

### 🧪 Pipeline

1. Load video  
2. Extract & preprocess frames  
3. TensorFlow classification  
4. Save abnormal frames  
5. YOLOv8 object detection  
6. Save annotated outputs  

---

## 🧠 Model Details

### TensorFlow
- **Input**: `(224, 224, 3)`
- **Output**: 0–1 abnormality score
- **Thresholding**: default = 0.5

### YOLOv8
- **Format**: `.pt` weights
- **Input size**: auto-scaled (default: 640x640)
- **Output**: bounding boxes, class, confidence

---

## 📁 Output Structure

```
output_directory/
├── abnormal_frames/
│   ├── abnormal_frame_0001.jpg
│   └── ...
└── yolo_output/
    ├── abnormal_frame_0001_detected.jpg
    └── ...
```

---

## 🛠️ Configuration Options

- **Abnormal Threshold**: 1–99% (default: 50%)
- **Frame Skip Interval**: 1–30 (default: 5)
- **YOLO Confidence**: 10–90% (default: 30%)
- **Preview**: real-time abnormal markers

---

## ⚡ Performance Tips

- **RAM Usage**: scales with resolution & batch size
- **Speed**: affected by hardware & skip interval
- **Storage**: JPEG outputs may grow rapidly

---

## 🧩 Troubleshooting

### 🧠 Model Errors
- Check for `zline_vs_esophagitis_model.h5` presence
- Ensure TensorFlow version matches

### 🎞️ Video Issues
- Unsupported format?
- Disk space?
- Corrupted input?

### 🔍 YOLO Issues
- Missing `best.pt`?
- Install `ultralytics`?
- Too few abnormal frames?

Use console logs for error tracing.

---

## 👥 Team Members

- **Muhammad Nasser**
- **Abdelrahman Emad**
- **Farah Yehia**
- **Alaa Essam**
- **Amat Elrahman**

---

## 🤝 Contributing

- Follow medical AI guidelines
- Test changes thoroughly
- Maintain compatibility with model formats
- Clearly document any updates

---

## 📜 License

Intended for **research and educational use only**. Comply with medical device and data privacy regulations when applied in clinical settings.

---

## 🆘 Support

For help, refer to:
- Documentation
- GitHub issues section
