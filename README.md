# face_recognition

This code is a face recognition part of my Sara project

First make a folder named registered and a folder inside with the name pre

Modules:
1. cv_version: 
Purpose: Combines face detection, registration, and recognition using OpenCV and face_recognition libraries.
Key Features:
- Uses OpenCV's Haar Cascade for initial face detection.
- Allows registering new faces by capturing 50 samples via webcam and saving them in a specified directory.
- Performs face recognition by comparing detected faces with pre-registered faces using the face_recognition library.
- Displays live video feed with bounding boxes around detected faces and labels recognized individuals.
- Automatically registers unknown faces by prompting for a name and capturing samples.
Components:
face_extractor(): Detects and crops faces from frames.
Make_Folder(): Creates a directory for new face samples.
Main loop: Continuously captures video, detects/recognizes faces, and handles new registrations

2. data_collecter.py
Purpose: Dedicated script for collecting face samples for registration.
Key Features:
- Captures 50 face samples via webcam using Haar Cascade for detection.
- Saves samples in a structured directory (registered/<name>/).
- Displays live count of captured samples on the cropped face image.
Components:
face_extractor(): Crops detected faces from frames.
Main loop: Captures frames, extracts faces, and saves them until 50 samples are collected or the user presses Enter.

3. face_recognition.py
Purpose: Standalone face recognition system.
Key Features:
- Compares detected faces with pre-registered faces in the registered/ directory.
- Labels recognized faces in real-time or marks them as "unknown".
- Uses face_recognition library for encoding and comparison.
Components:
Loads known face encodings and names at startup.
Main loop: Processes webcam feed, detects faces, and displays recognition results.


