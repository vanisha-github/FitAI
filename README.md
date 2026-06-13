# FitAI: Real-Time Exercise Form Analysis

FitAI is an AI-powered fitness monitoring platform that uses computer vision and pose estimation to analyze exercise form in real time. The system tracks body movements through a webcam, counts repetitions, evaluates exercise posture, and provides workout analytics through an interactive web interface.

## Live Demo

🔗 **Website:** [(https://gymwithai.netlify.app/)](https://gymwithai.netlify.app/)

## Features

* Real-time exercise form analysis using computer vision
* Automatic repetition counting
* Exercise posture evaluation
* Support for multiple exercises:

  * Squats
  * Push-Ups
  * Bicep Curls
* Pose estimation using MediaPipe
* Live webcam streaming with WebRTC
* Workout session tracking and analytics
* SQLite-based data storage
* Interactive Streamlit dashboard

## Tech Stack

**Frontend**

* Streamlit

**Computer Vision**

* OpenCV
* MediaPipe

**Real-Time Communication**

* WebRTC
* streamlit-webrtc

**Backend**

* Python

**Database**

* SQLite

**Libraries**

* NumPy

## System Workflow

1. Webcam captures the user's movement.
2. WebRTC streams video frames for processing.
3. MediaPipe extracts body landmarks in real time.
4. Exercise-specific detectors analyze body posture and joint angles.
5. Repetitions and workout metrics are computed.
6. Results are displayed instantly on the dashboard.
7. Exercise history and performance data are stored in SQLite.

## Supported Exercises

### Squats

* Knee angle tracking
* Hip movement analysis
* Automatic repetition counting

### Push-Ups

* Elbow angle monitoring
* Motion validation
* Repetition counting

### Bicep Curls

* Arm flexion tracking
* Angle-based movement detection
* Repetition counting

## Project Structure

```text
FitAI/
│
├── app.py
├── pages/
├── detectors/
│   ├── squat.py
│   ├── pushup.py
│   └── biceps_curl.py
│
├── services/
│   ├── config/
│   ├── persistence/
│   └── video/
│
├── data.db
├── assets/
└── requirements.txt
```

## Installation

### Clone Repository

```bash
git clone <repository-url>
cd FitAI
```

### Create Virtual Environment

```bash
python -m venv venv
```

### Activate Environment

**Windows**

```bash
venv\Scripts\activate
```

**Linux/macOS**

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

## Run the Application

```bash
streamlit run app.py
```

The application will be available at:

```text
http://localhost:8501
```

## Future Enhancements

* Additional exercise support
* AI-based posture correction feedback
* Personalized workout recommendations
* User authentication and profiles
* Cloud database integration
* Performance trend visualization
* Mobile application support
