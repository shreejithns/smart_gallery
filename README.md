# 🧠 AI-Powered Smart Gallery with Face Recognition (Self-Hosted Google Photos Alternative)

Welcome to **SmartGallery** — a private, AI-driven photo management system built with Django and InsightFace. I created this as a self-hosted alternative to Google Photos, offering intelligent photo organization powered by facial recognition, event grouping, and visual search.

---

## 🚀 Key Features

This is more than just a photo uploader — it’s a full-featured **Digital Asset Management (DAM)** system enhanced by AI.

### 👥 Face Recognition & Clustering
- Automatically detects and groups faces in every uploaded photo.
- Uses **InsightFace** and **DBSCAN + Cosine Similarity** to cluster identities — no manual tagging required.

### 🔍 Visual Search (Google Lens Style)
- Upload a selfie or cropped face and instantly find all matching photos in your gallery.

### 📅 Smart Event Grouping
- Groups uploads into “Events” (e.g., *Sunday Wedding*) based on timestamps and temporal clustering.

### 🖼️ AI-Powered Collage Generator
- Creates face-aware collages using OpenCV.
- Cropping respects face coordinates to avoid cutting off heads — 90% better accuracy vs traditional tools.

---

## 🛠 Tech Stack

| Layer               | Technologies Used                                               |
|---------------------|-----------------------------------------------------------------|
| Backend             | Django 5.0 (Python)                                             |
| AI Engine           | InsightFace (Buffalo_L), ONNX Runtime                          |
| Machine Learning    | Scikit-Learn (DBSCAN Clustering)                               |
| Computer Vision     | OpenCV, Pillow (PIL)                                           |
| Frontend            | HTML5, CSS3 (Glassmorphism UI), JavaScript                    |
| Task Management     | Threading (scalable to Celery + Redis)                        |

---

## 🧠 How It Works

### 1. **Face Embedding**
Each uploaded image is passed through InsightFace to extract a **512-dimensional face vector**.

### 2. **Incremental Learning**
New vectors are compared to existing group centroids. If the match is strong, it's assigned to a known profile instantly.

### 3. **Density Clustering**
For batch analysis (“Rescan”), DBSCAN clusters all face vectors to group unknown identities.

---

## 🔮 Future Enhancements

- 🗣️ **Natural Language Search** with CLIP (OpenAI)
- 🎥 **Video Facial Recognition**
- 📱 **Mobile App Sync** (Flutter or React Native)

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/ai-smart-gallery.git
cd ai-smart-gallery
```

### 2. Install Requirements

```bash
pip install -r requirements.txt
```

### 3. Download InsightFace Model

Download the **Buffalo_L** model from [InsightFace GitHub](https://github.com/deepinsight/insightface)  
Place it in the `/models/` directory.

### 4. Run the App

```bash
python manage.py runserver
```

---

## ⚙️ Prerequisites

- Python 3.10+
- A CUDA-capable GPU (optional, for acceleration)
- ONNX Runtime
- Django, OpenCV, Pillow, Scikit-learn, etc. (via `requirements.txt`)

---

## 📂 Folder Structure

```
├── ai_smart_gallery/
│   ├── core/
│   ├── templates/
│   ├── static/
│   ├── models/
│   └── media/
├── manage.py
├── requirements.txt
└── README.md
```

---

## 📸 Demo Screenshots

Coming soon...

---

## 📜 LICENSE

This project is released under the **MIT License**.

---

## 🙋‍♂️ AUTHOR

Built with ❤️ by **Shreejith N S**  
🔗 [linkedin.com/in/shreejithnsdev](https://linkedin.com/in/shreejithnsdev)  
💻 [github.com/shreejithns](https://github.com/shreejithns)

---

## 🤝 CONTRIBUTIONS

Feel free to fork, open issues, and submit PRs to enhance this project!
