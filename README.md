

This project is a Face Recognition Attendance System that captures real-time facial images, registers users, and keeps track of attendance using a webcam. Built with Flask, OpenCV, and machine learning, it enables automated attendance based on face recognition using K-Nearest Neighbors (KNN).

Table of Contents
Overview
Features
Installation
Usage
File Structure
Contributing
License
Overview
This application captures user images, trains a face recognition model, and stores attendance records. Users are registered with unique names and IDs, and attendance is automatically recorded upon recognition of a registered face.

Features
User Registration: Register new users with facial images captured from the webcam.
Real-Time Face Recognition: Uses K-Nearest Neighbors to recognize faces in real-time.
Attendance Logging: Automatically logs attendance to a CSV file based on recognized faces.
Flask Web Interface: Provides a user-friendly web interface for adding users, viewing attendance, and listing users.
Installation
Prerequisites
Python 3.6 or later
Flask
OpenCV
scikit-learn
Numpy
Pandas
Joblib
Steps
Clone this repository:

bash
Copy code
git clone https://github.com/deevanshdutta/show_project2-face-recognition-attendance.git
Navigate to the project directory:

bash
Copy code
cd show_project2-face-recognition-attendance
Install required packages:

bash
Copy code
pip install -r requirements.txt
Make sure the haarcascade_frontalface_default.xml file is in the root directory.

Start the Flask application:

bash
Copy code
python app.py
Usage
Go to http://127.0.0.1:5000 in your web browser.
Add a New User: Go to /add to register a new user. Enter a name and roll number, and capture images using the webcam.
Take Attendance: Click on the "Take Attendance" button to activate face recognition and log attendance.
List Users: View registered users and delete users if needed.
File Structure
app.py: Main application file for running the Flask server.
static/faces/: Directory containing registered user face images.
Attendance/: Folder for attendance CSV files.
templates/: HTML templates for the web interface.
haarcascade_frontalface_default.xml: OpenCV Haar Cascade for face detection.
Model Training
The model uses K-Nearest Neighbors (KNN) with n_neighbors=5 to classify registered faces. The training process is triggered upon adding a new user, and the trained model is saved as face_recognition_model.pkl in the static directory.
