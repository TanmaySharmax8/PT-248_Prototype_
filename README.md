# Smart ICU Patient Bed Safety & Automated Fall-Risk Monitoring System

A camera-based movement monitoring prototype designed to demonstrate how movement intensity can be monitored around an ICU patient bed and classified into different movement levels.

## 📌 Project Overview

Patient falls in Intensive Care Units (ICUs) are a major patient-safety concern. Continuous manual monitoring can be challenging for healthcare staff, particularly when multiple patients require attention.

This project presents an academic prototype that uses a webcam and browser-based image processing to estimate movement in a monitored area. It converts changes between consecutive video frames into a movement score and displays Low, Medium, or High movement levels.

The prototype demonstrates the basic concept of automated patient movement monitoring. It is not a clinically validated fall-prediction system.

## 🎯 Objectives

- Demonstrate camera-based movement monitoring.
- Estimate movement intensity using consecutive video frames.
- Generate a movement score ranging from 0 to 100.
- Classify movement into Low, Medium, and High levels.
- Allow users to adjust movement thresholds.
- Display the duration of continuous high-movement activity.
- Maintain a local event log of movement-level changes.
- Explore the potential of technology to support ICU patient safety.

## ✨ Features

- **Live Camera Feed:** Accesses the device camera through the browser.
- **Movement Detection:** Compares consecutive video frames to estimate changes in the monitored scene.
- **Movement Score:** Displays a movement score from 0 to 100.
- **Risk-Level Display:** Shows Low, Medium, or High movement levels using configurable thresholds.
- **Adjustable Thresholds:** Allows users to modify the Medium and High movement thresholds.
- **High-Movement Duration:** Tracks how long the detected movement remains at the High level.
- **Event Logging:** Records movement-level changes locally on the page.
- **Baseline Reset:** Resets the movement comparison baseline.
- **Camera Controls:** Allows monitoring to be started and stopped.
- **Privacy-Oriented Prototype:** Processes video frames within the browser and does not upload or save video through the prototype.

## 🛠️ Technologies Used

- HTML5 — Structure of the application.
- CSS3 — User interface and responsive styling.
- JavaScript — Camera control, frame comparison, movement scoring, and event logging.
- Browser MediaDevices API — Webcam access.
- HTML Canvas API — Sampling and processing video frames.
- requestAnimationFrame — Repeated frame processing.
- Google Chrome or Microsoft Edge — Recommended browsers for running the prototype.

No external JavaScript libraries, database, or backend server are required for the current prototype.

## 📂 Project Structure

```text
smart-icu-patient-bed-safety/
│
├── smart_icu_movement_prototype.html
└── README.md
```

## ⚙️ How It Works

1. The user starts the camera and grants permission.
2. The application captures video frames from the webcam.
3. A small canvas is used to sample each frame at a resolution of 160 × 90 pixels.
4. The application compares grayscale pixel values between consecutive frames.
5. The observed differences are converted into a smoothed movement score between 0 and 100.
6. Configurable thresholds determine the Low, Medium, or High movement level.
7. The interface displays the current movement assessment and high-movement duration.
8. Changes in movement level are recorded in the local event log.

### Movement Classification

- **Low:** Movement score is below the Medium threshold.
- **Medium:** Movement score reaches the Medium threshold but remains below the High threshold.
- **High:** Movement score reaches or exceeds the High threshold.

The default Medium threshold is 18, and the default High threshold is 38. These values are adjustable and are demonstration settings, not medically validated thresholds.

## 🚀 How to Run the Project

### Requirements

- A computer with a webcam.
- A modern web browser.
- Python installed if using the local-server method.

### Method 1: Run Using a Local Server (Recommended)

1. Clone or download this repository.
2. Open the project folder in a terminal.
3. Start a local server using:

   ```bash
   python -m http.server 8000
   ```

4. Open the following address in your browser:

   `http://localhost:8000/smart_icu_movement_prototype.html`

5. Click **Start camera** and allow camera permission.
6. Observe the movement score, movement classification, duration, and event log.
7. Use **Stop camera** to end monitoring.

If Python is installed through the Windows Python Launcher, `py -m http.server 8000` can also be used.

### Method 2: Open the HTML File Directly

Open `smart_icu_movement_prototype.html` in a modern browser. Camera access may be restricted when the file is opened directly, so the local-server method is recommended.

## 🧪 Testing

The prototype can be tested by:

- Starting and stopping the webcam.
- Moving within the camera's field of view.
- Observing changes in the movement score.
- Adjusting the Medium and High thresholds.
- Checking the high-movement duration.
- Verifying that movement-level changes appear in the event log.
- Resetting the baseline and clearing the event log.
- Testing under different lighting conditions.

Results may vary depending on camera placement, lighting, background movement, and scene changes.

## ⚠️ Limitations and Safety Disclaimer

- This is an academic demonstration prototype.
- Movement intensity alone cannot determine whether a patient is about to fall or has exited the bed.
- Camera movement, lighting changes, visitors, and bedding motion can affect the movement score.
- The system does not currently perform patient pose estimation, trained machine-learning inference, or medically validated fall-risk prediction.
- The current prototype does not integrate bed sensors, a hospital database, cloud storage, or automatic nurse notifications.
- The event log is maintained in the current web page and is not a persistent database.
- Camera access requires browser permission and an appropriate secure context, such as localhost or HTTPS.

**This prototype must not be used for clinical decisions or as a replacement for professional supervision, hospital safety procedures, or validated medical equipment.**

## 🔮 Future Scope

Possible future improvements include:

- Integration of computer-vision models for patient pose estimation.
- Detection of bed-exit attempts using more advanced movement analysis.
- Integration with pressure, occupancy, or proximity sensors.
- Real-time notifications for authorized healthcare staff.
- Persistent event storage and performance reporting.
- Secure remote monitoring and access control.
- Testing and validation under appropriate clinical supervision.

These are proposed enhancements and are not implemented in the current version.

## 🎓 Project Information

**Project Title:** Smart ICU Patient Bed Safety & Automated Fall-Risk Monitoring System

**Project Type:** Academic Major Project — Phase I

**Domain:** Healthcare Technology, Web Development, Computer Vision

**Institution:** IILM University, Greater Noida

**Academic Session:** 2026–27

### Project Team

- Arpit Negi
- Anvesha
- Yash Tyagi
- Tanmay

### Project Guide

Jyoti Kataria

## 📄 License

No open-source license has been specified for this project yet. All rights are reserved by default unless a license is added.

## 🤝 Contributions

This repository documents an academic prototype. Suggestions and improvements are welcome, provided they accurately distinguish implemented functionality from proposed future features.
