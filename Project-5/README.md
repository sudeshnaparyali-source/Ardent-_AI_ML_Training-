# 😊 Real-Time Emotion Detection System

A real-time facial emotion detection application built with OpenCV and a custom-trained deep learning model. The system uses your webcam to detect faces and classify emotions live — no cloud APIs or third-party services required.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green?logo=opencv)
![Keras](https://img.shields.io/badge/Keras-TensorFlow-red?logo=keras)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

## 🎯 Features

- **Real-time detection** — processes webcam feed frame-by-frame with no perceptible lag
- **7 emotion classes** — Angry, Disgust, Fear, Happy, Sad, Surprise, Neutral
- **Lightweight** — runs entirely on-device using a compact `.hdf5` model, no internet connection needed
- **Mac compatible** — uses `cv2.CAP_AVFOUNDATION` for native macOS webcam support
- **Haar Cascade face detection** — fast and reliable frontal face localization

---

## 🗂️ Project Structure

```
emotion-detection/
│
├── emotion_detection.py                  # Main application script
├── emotion_model.hdf5                    # Pre-trained emotion classification model
├── haarcascade_frontalface_default.xml   # OpenCV face detection model
└── README.md
```

---

## 🧠 How It Works

1. **Face Detection** — Each video frame is converted to grayscale and passed through OpenCV's Haar Cascade classifier to locate faces.
2. **Preprocessing** — Detected face regions are resized to `64×64` pixels and normalized to `[0, 1]`.
3. **Emotion Classification** — The preprocessed ROI is fed into a Keras CNN model (`emotion_model.hdf5`) which outputs a probability distribution over 7 emotion classes.
4. **Visualization** — A bounding box and the predicted emotion label are drawn on the original frame in real time.

---

## 🛠️ Requirements

- Python 3.8+
- OpenCV
- NumPy
- TensorFlow / Keras

Install dependencies:

```bash
pip install opencv-python numpy tensorflow
```

---

## 🚀 Getting Started

**1. Clone the repository:**

```bash
git clone https://github.com/your-username/emotion-detection.git
cd emotion-detection
```

**2. Ensure all required files are present:**

- `emotion_model.hdf5`
- `haarcascade_frontalface_default.xml`
- `emotion_detection.py`

**3. Run the application:**

```bash
python emotion_detection.py
```

**4. Press `q` to quit.**

---

## 📊 Emotion Classes

| Index | Emotion  |
|-------|----------|
| 0     | Angry    |
| 1     | Disgust  |
| 2     | Fear     |
| 3     | Happy    |
| 4     | Sad      |
| 5     | Surprise |
| 6     | Neutral  |

---

## ⚙️ Configuration

| Parameter | Default | Description |
|-----------|---------|-------------|
| Input size | `64×64` | Face ROI dimensions fed to the model |
| Scale factor | `1.3` | Haar Cascade detection sensitivity |
| Min neighbors | `5` | Minimum neighboring detections to confirm a face |
| Camera backend | `CAP_AVFOUNDATION` | macOS-native backend (change to `0` for Linux/Windows) |

**For Linux or Windows**, update the capture line in `emotion_detection.py`:

```python
# Replace this:
cap = cv2.VideoCapture(0, cv2.CAP_AVFOUNDATION)

# With this:
cap = cv2.VideoCapture(0)
```

---

## 🔮 Future Improvements

- [ ] Add confidence score display alongside emotion label
- [ ] Support for multiple simultaneous face tracking
- [ ] Export detected emotions to a log file with timestamps
- [ ] Build a GUI dashboard with emotion history chart
- [ ] Train on a larger dataset (e.g., AffectNet) for improved accuracy

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgements

- [OpenCV](https://opencv.org/) for real-time computer vision tools
- [Keras](https://keras.io/) for the deep learning framework
- The FER-2013 dataset community for advancing emotion recognition research
