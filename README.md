# Speed-Detection-System-Using-AI-and-Computer-Vision
🚗 Speed Detection System Using AI &amp; Computer Vision A real-time traffic monitoring system utilizing YOLO object detection, OpenCV, and MySQL to track vehicle speeds, detect violations, and log cases securely. Features automatic image capture, JWT authentication, and session management for secure, efficient speed monitoring.


Speed Detection System Using AI and Computer Vision
🚗 AI-Powered Speed Monitoring for Traffic Safety 🚦
Overview
This project is a real-time speed detection system that utilizes computer vision, artificial intelligence (AI), and MySQL databases to track and analyze vehicle speeds. The system employs YOLO (You Only Look Once) object detection, OpenCV for image processing, and MySQL for case logging, ensuring efficient monitoring of road traffic and identifying speed violations.

Features
✅ Real-time vehicle detection using YOLO ✅ Speed estimation through object tracking ✅ Automatic image capture for over-speeding vehicles ✅ Case logging in MySQL database ✅ Session management and authentication ✅ Optimized for highway and urban traffic monitoring

How It Works
1. Object Detection Using YOLO
The system initializes the YOLOv8 model, trained to identify various objects, including cars, trucks, buses, and motorbikes.

A video feed from a camera or recorded footage is processed frame-by-frame.

YOLO detects vehicles by drawing bounding boxes around them and assigning unique IDs for tracking.

2. Vehicle Tracking & Speed Calculation
Sort Algorithm is used to track vehicles as they move through the frame.

When a vehicle crosses predefined detection lines, the system records timestamps.

Using distance and time calculations, the system estimates vehicle speed (km/h).

If a vehicle exceeds the speed limit, its bounding box is captured and stored as evidence.

3. Case Logging with MySQL
The system logs each speed violation into a MySQL database with key data:

Car ID, entry time, exit time, estimated speed, location, and a captured image.

SQL queries are executed to store and retrieve cases, ensuring organized record-keeping.


Technology Stack
Programming Language: Python

AI Model: YOLOv8 (Ultralytics)

Computer Vision: OpenCV, CVZone

Database Management: MySQL

Object Tracking: SORT Algorithm

Authentication: JWT

Automated Emails: SMTP

Installation & Setup
1. Clone the Repository
bash
git clone https://github.com/yourusername/speed-detection.git
cd speed-detection
2. Install Dependencies
bash
pip install numpy opencv-python cvzone mysql-connector-python ultralytics
3. Configure MySQL Database
Set up a MySQL database named speed_detection_db.

Create a table case_tb with columns:

sql
CREATE TABLE case_tb (
    car_id INT PRIMARY KEY,
    entrance_time DATETIME,
    exit_time DATETIME,
    speed FLOAT,
    image_data BLOB,
    place VARCHAR(255),
    date DATETIME
);
Update connection details in the Python script.

4. Run the Speed Detection Script
bash
python speed_detection.py
Future Enhancements
🔹 Cloud Storage Integration for centralized logging 🔹 Real-time Web Dashboard for monitoring violations 🔹 Fine Processing System for automated penalty generation 🔹 Multi-Camera Support for large-scale deployment

Contributing
Feel free to fork this repository, submit pull requests, or suggest improvements!
