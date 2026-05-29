# VisionServo-Pi 

An automated, low-latency Pan-Tilt target tracking system driven by OpenCV computer vision on a Raspberry Pi Zero 2 W. 

This project isolates high-intensity light sources (like an LED or flashlight) using real-time image thresholding, calculates coordinate deltas, and drives physical hardware via a custom low-pass filter thread to achieve incredibly fluid mechanical motion.

##  Features
* **Real-Time LED Tracking:** Leverages OpenCV contour math and pixel brightness analysis to rapidly lock onto target positions.
* **Low-Latency Live Streaming:** Hosts a lightweight, concurrent MJPEG web streaming server natively on port `8000`.
* **Mechanical Smoothing Filter:** Implements a decoupled dual-thread architecture with a math-based Low-Pass Filter and Deadzone to eliminate servo jitter and aggressive over-correction.
* **180° Orientation Flip:** Preconfigured video matrix transformation to handle inverted hardware mounting schemas.

##  Hardware Requirements
* Raspberry Pi Zero 2 W (Running Debian Trixie / Pi OS)
* Raspberry Pi Camera Module (NoIR/Infrared recommended)
* 2x SG90 Micro Servo Motors (Pan/Tilt configuration)
* 5V External Power Source (Shared Common Ground with Pi GND)

