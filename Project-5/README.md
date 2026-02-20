😤😊😲 Real-Time Emotion Detection System

A real-time facial emotion recognition system built with Python, OpenCV, and a pre-trained Keras deep learning model — no DeepFace, no cloud API, runs entirely on your local webcam.


📌 About This Project
This project detects human emotions in real-time using your webcam. It combines classical computer vision (Haar Cascade face detection) with a deep learning model (CNN trained on facial expression data) to identify 7 emotions live, frame by frame.
Built as a hands-on AI/ML project to learn computer vision, model loading, and real-time inference pipelines.
Platform: Local machine (Mac-compatible via cv2.CAP_AVFOUNDATION)
Language: Python 3
Libraries: OpenCV, Keras/TensorFlow, NumPy

🎯 Detected Emotions
LabelEmotion😠Angry🤢Disgust😨Fear😄Happy😢Sad😲Surprise😐Neutral

🧠 How It Works
Webcam Frame
     ↓
Convert to Grayscale
     ↓
Haar Cascade → Detect Face(s)
     ↓
Crop & Resize ROI to 64×64
     ↓
Normalize pixel values (÷ 255)
     ↓
Reshape → (1, 64, 64, 1)
     ↓
CNN Model (emotion_model.hdf5) → Predict
     ↓
Argmax → Emotion Label
     ↓
Draw Bounding Box + Label on Frame
     ↓
Display Live via OpenCV Window

📂 Project Structure
📁 emotion-detection/
├── emotion_detection.py                 # Main script — webcam loop + inference
├── emotion_model.hdf5                   # Pre-trained CNN model (Keras)
├── haarcascade_frontalface_default.xml  # OpenCV face detector
└── README.md                            # This file

⚙️ Setup & Installation
1. Clone the Repository
bashgit clone https://github.com/your-username/emotion-detection.git
cd emotion-detection
2. Install Dependencies
bashpip install opencv-python numpy tensorflow keras

macOS users: cv2.CAP_AVFOUNDATION is already set in the script for native webcam support.
Windows/Linux users: Change this line in emotion_detection.py:
python# From:
cap = cv2.VideoCapture(0, cv2.CAP_AVFOUNDATION)
# To:
cap = cv2.VideoCapture(0)

3. Run the Script
bashpython emotion_detection.py
Press q to quit the live window.

🖥️ Demo
✅ Webcam opens
✅ Face detected → green bounding box drawn
✅ Emotion label displayed above the face in real-time
✅ Supports multiple faces in the same frame
✅ Press 'q' to exit cleanly

🔬 Technical Details
ComponentDetailsFace DetectionHaar Cascade Classifier (haarcascade_frontalface_default.xml)Model FormatKeras HDF5 (.hdf5) — loaded with compile=FalseInput Shape(1, 64, 64, 1) — grayscale, single channelNormalizationPixel values divided by 255.0 — range [0, 1]Predictionnp.argmax() on softmax output → emotion indexScale Factor1.3 with minNeighbors=5 for stable face detectionDisplaycv2.rectangle + cv2.putText overlay on live frame

📦 Dependencies
txtopencv-python
numpy
tensorflow
keras
Install all at once:
bashpip install opencv-python numpy tensorflow keras

⚠️ Known Limitations

Works best in good lighting conditions
Detection accuracy may drop with partial face occlusion (masks, angles)
haarcascade may produce false positives in cluttered backgrounds
Model performance depends on the training dataset it was built on


🎯 What I Learned

Loading and running a pre-trained Keras CNN model for inference
Using OpenCV Haar Cascades for real-time face detection
Building a complete frame-by-frame video processing loop
Preprocessing image ROIs: resize → normalize → reshape for model input
Drawing bounding boxes and text overlays on live video with OpenCV
Handling webcam compatibility across operating systems


🔮 Future Improvements

 Add confidence score display (e.g., Happy 94%)
 Log emotion history to a CSV file with timestamps
 Add support for image/video file input (not just webcam)
 Build a GUI dashboard using Tkinter or Streamlit
 Replace Haar Cascade with a DNN-based face detector for better accuracy


👤 Author
Student Name — B.Sc (CSE), Haldia Institute of Management
Mentored by: SK Sahil (AI Developer & Tutor) — @Code_ScholarEU

🐙 GitHub: https://github.com/your-username
📧 Email: your-email@example.com
📸 Instagram: @code_scholar_eu


📄 License
This project is open for personal and educational use. Feel free to fork and build upon it.

Built with Python 🐍 • OpenCV 👁️ • Keras 🧠 — Real-time AI, zero cloud dependency😤😊😲 Real-Time Emotion Detection System

A real-time facial emotion recognition system built with Python, OpenCV, and a pre-trained Keras deep learning model — no DeepFace, no cloud API, runs entirely on your local webcam.


📌 About This Project
This project detects human emotions in real-time using your webcam. It combines classical computer vision (Haar Cascade face detection) with a deep learning model (CNN trained on facial expression data) to identify 7 emotions live, frame by frame.
Built as a hands-on AI/ML project to learn computer vision, model loading, and real-time inference pipelines.
Platform: Local machine (Mac-compatible via cv2.CAP_AVFOUNDATION)
Language: Python 3
Libraries: OpenCV, Keras/TensorFlow, NumPy

🎯 Detected Emotions
LabelEmotion😠Angry🤢Disgust😨Fear😄Happy😢Sad😲Surprise😐Neutral

🧠 How It Works
Webcam Frame
     ↓
Convert to Grayscale
     ↓
Haar Cascade → Detect Face(s)
     ↓
Crop & Resize ROI to 64×64
     ↓
Normalize pixel values (÷ 255)
     ↓
Reshape → (1, 64, 64, 1)
     ↓
CNN Model (emotion_model.hdf5) → Predict
     ↓
Argmax → Emotion Label
     ↓
Draw Bounding Box + Label on Frame
     ↓
Display Live via OpenCV Window

📂 Project Structure
📁 emotion-detection/
├── emotion_detection.py                 # Main script — webcam loop + inference
├── emotion_model.hdf5                   # Pre-trained CNN model (Keras)
├── haarcascade_frontalface_default.xml  # OpenCV face detector
└── README.md                            # This file

⚙️ Setup & Installation
1. Clone the Repository
bashgit clone https://github.com/your-username/emotion-detection.git
cd emotion-detection
2. Install Dependencies
bashpip install opencv-python numpy tensorflow keras

macOS users: cv2.CAP_AVFOUNDATION is already set in the script for native webcam support.
Windows/Linux users: Change this line in emotion_detection.py:
python# From:
cap = cv2.VideoCapture(0, cv2.CAP_AVFOUNDATION)
# To:
cap = cv2.VideoCapture(0)

3. Run the Script
bashpython emotion_detection.py
Press q to quit the live window.

🖥️ Demo
<img width="740" height="798" alt="image" src="https://github.com/user-attachments/assets/57aed7de-f022-4bd1-9705-e0215f6c9c59" />

✅ Webcam opens
✅ Face detected → green bounding box drawn
✅ Emotion label displayed above the face in real-time
✅ Supports multiple faces in the same frame
✅ Press 'q' to exit cleanly

🔬 Technical Details
ComponentDetailsFace DetectionHaar Cascade Classifier (haarcascade_frontalface_default.xml)Model FormatKeras HDF5 (.hdf5) — loaded with compile=FalseInput Shape(1, 64, 64, 1) — grayscale, single channelNormalizationPixel values divided by 255.0 — range [0, 1]Predictionnp.argmax() on softmax output → emotion indexScale Factor1.3 with minNeighbors=5 for stable face detectionDisplaycv2.rectangle + cv2.putText overlay on live frame

📦 Dependencies
txtopencv-python
numpy
tensorflow
keras
Install all at once:
bashpip install opencv-python numpy tensorflow keras

⚠️ Known Limitations

Works best in good lighting conditions
Detection accuracy may drop with partial face occlusion (masks, angles)
haarcascade may produce false positives in cluttered backgrounds
Model performance depends on the training dataset it was built on


🎯 What I Learned

Loading and running a pre-trained Keras CNN model for inference
Using OpenCV Haar Cascades for real-time face detection
Building a complete frame-by-frame video processing loop
Preprocessing image ROIs: resize → normalize → reshape for model input
Drawing bounding boxes and text overlays on live video with OpenCV
Handling webcam compatibility across operating systems


🔮 Future Improvements

 Add confidence score display (e.g., Happy 94%)
 Log emotion history to a CSV file with timestamps
 Add support for image/video file input (not just webcam)
 Build a GUI dashboard using Tkinter or Streamlit
 Replace Haar Cascade with a DNN-based face detector for better accuracy


👤 Author
Student Name — B.Sc (CSE), Haldia Institute of Management
Mentored by: SK Sahil (AI Developer & Tutor) — @Code_ScholarEU

🐙 GitHub: https://github.com/your-username
📧 Email: your-email@example.com
📸 Instagram: @code_scholar_eu


📄 License
This project is open for personal and educational use. Feel free to fork and build upon it.

Built with Python 🐍 • OpenCV 👁️ • Keras 🧠 — Real-time AI, zero cloud dependency
