# Realtime Drowsiness Detection System

A Python-based project that detects driver drowsiness and yawning in real-time using a webcam. Built using `OpenCV`, `face_recognition`, `numpy`, and `scipy`.

## 🚀 Features

- Eye Aspect Ratio (EAR) based drowsiness detection
- Mouth Aspect Ratio (MAR) based yawning detection
- Alerts when:
  - Face is not detected for a duration
  - Camera is blocked or disconnected
- Red screen and beep sound for critical alerts
- Smooth UI using OpenCV display

## 🛠️ Technologies Used

- Python
- OpenCV
- dlib (via face_recognition)
- NumPy
- SciPy
- winsound (for beeping alerts)

## 📸 Working

1. **Face Detection**  
   Uses `face_recognition` to detect facial landmarks like eyes and mouth.

2. **Drowsiness Detection**  
   Calculates Eye Aspect Ratio (EAR). If EAR < threshold for a fixed duration, it triggers a **Drowsiness Warning** with red screen and sound alert.

3. **Yawning Detection**  
   Calculates Mouth Aspect Ratio (MAR). When MAR > threshold along with low EAR, it detects **Yawning**.

4. **Blocked Camera Alert**  
   Detects camera obstruction based on low brightness. Alerts with red screen and sound.

5. **Face Not Found Alert**  
   If the face is not detected for more than 3 seconds, it shows a "FULL FACE NOT FOUND!" warning.

6. **Camera Disconnection Handling**  
   Automatically detects and shows alert if the webcam is disconnected during runtime.

## 🔊 Sample Working

> The system uses visual cues and audio feedback to alert the user:
- Red screen + beep for **drowsiness**, **camera block**, **camera disconnect**, and **no face detected**
- On-screen message for **yawning detected**

## 🔮 Future Work

- Add logging for drowsiness/yawn events with timestamps
- Integrate with vehicle alert system (buzzer or seat vibration)
- Add support for multiple faces (passenger vs driver)
- Use deep learning models for more accurate detection
- Implement night mode support using infrared-based detection
- Build GUI with PyQt or Tkinter for better control panel

## 🧑‍💻 Developed By

**Naushaba Imroz**  
Intern at Tata Motors  
BTech CSE, VIT Vellore
