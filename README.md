<div align="center">

# 🎭 Live Emotion Detector - Train Your Own

**Record your own expressions with a webcam, train a small neural network on the landmarks and classify them live.**

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7?logo=google&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?logo=keras&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?logo=opencv&logoColor=white)

</div>

---

## ✨ How it works

1. 📷 **Collect data - `data.py`**: enter a label name; MediaPipe **Holistic** captures face and hand landmarks (coordinates relative to a reference point) from your webcam and saves them to a `<label>.npy` file (e.g. `yes.npy`, `no.npy`).
2. 🧠 **Train - `train.ipynb`**: loads the `.npy` files, builds a Keras dense network and trains it for 50 epochs (accuracy ≈ 90 %). The model is saved as `model.h5` and the class names as `labels.npy`.
3. 🎥 **Run live - `s.py`**: classifies each webcam frame and draws the predicted label on the video.

Because you record the samples yourself, you can train it on any expressions or gestures you like.

## 🚀 Getting Started

```bash
git clone https://github.com/Arashomranpour/live-emotion-detector-with-training-.git
cd live-emotion-detector-with-training-
pip install opencv-python mediapipe tensorflow keras numpy pandas jupyter

python data.py        # run once per label (e.g. "yes", "no")
jupyter notebook train.ipynb
python s.py           # live prediction
```

## 📁 Project Structure

```
.
├── data.py          # Record landmark samples for a label
├── train.ipynb      # Train and save the classifier
├── s.py             # Live inference
├── model.h5         # Trained model
└── labels.npy  yes.npy  no.npy   # Class names and sample data
```

## 🛠️ Tech Stack

`MediaPipe` · `OpenCV` · `Keras / TensorFlow` · `NumPy`
