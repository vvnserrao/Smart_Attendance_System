# Face Recognition Based Smart Attendance System

## Overview

The Face Recognition Based Smart Attendance System is designed to automate attendance tracking using face recognition technology. This system identifies individuals from live video feeds and records their attendance accurately and efficiently, making it suitable for schools, businesses, and other organizations.

## Objectives

- Implement Face Recognition Technology
- Facilitate Seamless Integration
- Automate Attendance Tracking
- Enhance Accuracy and Efficiency

## Features

- **Face Encoding**: Extracts and encodes facial features from images.
- **Real-Time Attendance Logging**: Recognizes faces in live video and logs attendance with timestamps.
- **Attendance Records**: Maintains attendance records in CSV format, organized by date.

## Tools and Technologies

- **Programming Language**: Python
- **Libraries**:
  - OpenCV (Open Source Computer Vision Library)
  - NumPy (Numerical Python)
  - face_recognition Library
  - Threading Module

## Functionality

### Encode Faces Function

```python
def encode_faces():
    encoded_data = {}
    for dirpath, dnames, fnames in os.walk("./Images"):
        for f in fnames:
            if f.endswith(".jpg") or f.endswith(".png"):
                face = fr.load_image_file("Images/" + f)
                encoding = fr.face_encodings(face)[0]
                encoded_data[f.split(".")[0]] = encoding
    return encoded_data
```
- Extracts facial features from images in the designated directory.
- Uses the face_recognition library to encode faces, generating unique representations for each individual.
- Enables accurate identification of individuals within the attendance system.

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project directory:
   ```bash
   cd Smart_Attendance_System
   ```
3. Install the required Python libraries:
   ```bash
   pip install opencv-python numpy face_recognition
   ```
4. Ensure you have a directory named `Images` containing the images of individuals to be recognized.
5. Run the application:
   ```bash
   python main.py
   ```

## Usage

1. Start the application.
2. The system will use the webcam to capture live video.
3. It will recognize faces from the video feed and log attendance with timestamps in a CSV file.


---
