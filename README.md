# AGRIWEED


Here’s a README file that you can use for your GitHub repository. It’s designed to provide a comprehensive overview of your autonomous inter-row weed removal project, explaining its purpose, setup, and usage.

Autonomous Inter-Row Weed Removal System
This project is an Autonomous Inter-Row Weed Removal System that uses computer vision and robotics to detect and remove weeds from agricultural fields. The system leverages a YOLO-based object detection model to identify weeds among crops in real time and directs a delta robot to remove them. The project aims to reduce the need for manual weeding, helping farmers save time and effort in maintaining crop health.

Table of Contents
Features
Technologies Used
System Architecture
Installation
Usage
Directory Structure
Contributing
License
Features
Real-time weed detection using YOLO.
Delta robot controlled via Arduino to autonomously remove detected weeds.
Video streaming of detection results for monitoring.
Flexible control via a web interface, with commands sent to the robot for precise movement.
Technologies Used
Python: For the main application and server.
Flask: To create a web server for video streaming and command control.
OpenCV: For capturing video, processing frames, and drawing detection results.
Roboflow: For object detection using a YOLO model.
Arduino: To control the delta robot’s movements based on weed detection.
HTML/CSS/JavaScript: For creating the web interface.
System Architecture
Weed Detection: Video frames are captured from the camera and processed using a YOLO model on Roboflow's platform.
Robot Control: Weed detection results are sent to an Arduino-controlled delta robot, which positions itself to remove detected weeds.
Web Interface: A Flask-based web interface streams live video of the detection results and allows users to monitor the process.
Installation
Prerequisites
Python 3.8+
Arduino IDE
Roboflow API key (sign up on Roboflow and get an API key)
OpenCV, Flask, and other Python dependencies (see below)
Setup Instructions
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/inter-row-weed-removal.git
cd inter-row-weed-removal
Install dependencies:

bash
Copy code
pip install -r requirements.txt
The requirements.txt should include opencv-python, flask, roboflow, and pyserial.

Set up Arduino:

Open the Arduino file (robot_controller.ino) in the Arduino IDE.
Upload the code to the Arduino board.
Make sure the Arduino board is connected to your computer's appropriate COM port.
Configure Roboflow:


Usage
Run the Flask server:

bash
Copy code
python app.py
This will start the web server on http://127.0.0.1:5000.

Access the Web Interface:

Open a web browser and go to http://127.0.0.1:5000 to view the live video feed.
The video feed displays bounding boxes and labels for detected weeds.
Use the web interface to send control commands to the delta robot if needed.
Monitor the Delta Robot:

The robot will automatically move to the weed coordinates and perform weed removal actions as detected by the model.
