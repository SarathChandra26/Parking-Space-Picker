# 🚗 Parking Space Picker – Computer Vision Project

Parking Space Picker is a real-time computer vision system that detects and counts available parking spaces from video footage using image processing techniques. It is designed to demonstrate how OpenCV can be used to solve real-world smart city and parking management problems.

---

## 🔍 Project Overview

This project analyzes a parking lot video feed and determines which parking slots are occupied or free. Each parking space is pre-defined, and the system continuously monitors the area to provide real-time availability information.

The project is ideal for learning:
- Computer Vision fundamentals
- Image preprocessing techniques
- Real-time video analysis
- Smart parking system concepts

---

## ⚙️ How It Works

1. A parking lot video (`carPark.mp4`) is used as the input.
2. Parking slot positions are manually selected and stored using a pickle file (`CarParkPos.pkl`).
3. Each video frame undergoes preprocessing:
   - Grayscale conversion
   - Gaussian blur
   - Adaptive thresholding
   - Median blur
   - Dilation
4. Pixel intensity is analyzed inside each parking slot:
   - Fewer white pixels → Slot is **empty**
   - More white pixels → Slot is **occupied**
5. Bounding boxes are drawn:
   - 🟢 Green → Available space
   - 🔴 Red → Occupied space
6. The total number of free parking spaces is displayed in real time.

---

## ✨ Features

- 📹 Real-time parking space detection
- 🟢🟥 Visual indicators for free and occupied slots
- 🔢 Live counter for available parking spaces
- ⚡ Fast and lightweight processing
- 🧠 No deep learning required (pure OpenCV logic)

---

## 🛠️ Technologies Used

- **Python**
- **OpenCV**
- **NumPy**
- **cvzone**
- **Pickle (for parking slot storage)**

---

## 📁 Project Structure

```text
ParkingSpacePicker/
│
├── main.py                 # Main application logic
├── ParkingSpacePicker.py   # Parking space selection utility
├── CarParkPos.pkl          # Stored parking slot coordinates
├── carPark.mp4             # Input video
├── carParkImg.png          # Reference image
└── README.md
