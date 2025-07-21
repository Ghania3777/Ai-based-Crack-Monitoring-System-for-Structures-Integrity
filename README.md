# Ai-based-Crack-Monitoring-System-for-Structures-Integrity
# SOFTWARE INTEGRATION
Our developed system will integrate AI technologies, such as machine learning and image processing to monitor cracks.
This project performs real-time object detection and segmentation using the YOLOv8 model. It is trained on a custom and standard datasets and can detect and segment cracks in images.
# Tools and Libraries Used
YOLOv8 (Ultralytics)
Python
PyTorch
Google Colab (for training, validation,testing)
Custom and Standard datasets in YOLO format

# Datasets
We used a standatd dataset labeled them manually using roboflow and also used custom dataset(also labeled them manually) in YOLO format. The dataset contains images and their labels for both object detection and segmentation.

# Results
The model was trained for 50 epochs. The validation mAP was good, and the model is able to detect and segment objects accurately.

# HARDWARE INTEGRATION
This system integrates hardware and software components for real-time crack detection using a drone, Raspberry Pi, and a deployed YOLOv8 model.
# Workflow Overview:
1. Image Capture via Drone
A drone equipped with a camera captures images of infrastructure surfaces.

2. Mobile App (HTTP Request Shortcuts)
The captured image is sent to the Raspberry Pi using a mobile app that makes an HTTP request to the Flask server running on the Pi.

3. Raspberry Pi with Flask Server
The Pi receives the image using its IP or hostname. The Flask server handles the image upload and forwards it for processing.

4. YOLOv8 Model Inference (on Pi)
The image is processed locally on the Raspberry Pi using a pre-trained YOLOv8 model for crack detection and segmentation.

5. Sending Results Back
The detection results are returned as a response to the mobile app, showing bounding boxes or segmentation masks on the image.

# Hardware Used:
DJI Mini Drone – For aerial image capture.

Raspberry Pi 5 Model B – Hosts the Flask server and YOLOv8 model.

Mobile Device – Runs HTTP Shortcuts app to communicate with the Pi.

MicroSD Card (32GB) – Stores the OS, scripts, and trained models.

Battery Pack / Power Bank – Powers the Raspberry Pi in field conditions.
