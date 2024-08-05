centre-tracker

 Real-Time Object Tracking with Center:
This project aims to implement real-time object tracking using a webcam, where the center point of the tracked object is continuously displayed. The tracking is facilitated using OpenCV's CSRT (Channel and Spatial Reliability Tracker) or KCF (Kernelized Correlation Filters) tracker.
 Project Details:
Objective: To create a system that can track an object in real-time using a webcam and highlight its center point.
Components:
•	Real-time video feed from a webcam.
•	Object tracking algorithm (CSRT or KCF).
•	Display of the tracked object's center point.

 System Requirements:
Operating System: Windows, macOS, or Linux
Hardware:
  - Webcam
  - At least 4GB of RAM
  - Modern CPU (Intel i5 or equivalent)
Software:
  - Python 3.6 or higher
  - OpenCV
  - PyTorch (for YOLOv8 training)
  - LabelImg (for annotation)

Install the Required Libraries:
You can install the required Python libraries using `pip`. Open your terminal or command prompt and run:
•	pip install opencv-python-headless
•	pip install torch torchvision
•	pip install labelImg
•	pip install Numpy
•	pip install pyTorch
•	pip install opencv

   Label the Data:
•	Open your images in LabelImg.
•	Draw bounding boxes around the objects you want to track and assign labels.
•	Save the annotations in YOLO format.
Training YOLOv8
To train YOLOv8, you will need to follow these steps:
Prepare Your Dataset:
•	Ensure your images and labels are correctly formatted and organized.
•	Split your dataset into training and validation sets.
Download and Setup YOLOv8:
•	Clone the YOLOv8 repository:
                  bash
                  git clone https://github.com/ultralytics/yolov8
                  cd yolov8

•	Install dependencies:
                 bash
                 pip install -r requirements.txt


•	Train the Model:
   bash
   python train.py --data path/to/your/dataset --cfg yolov8.yaml --weights '' --name      yolov8_custom
    Monitor Training:
During training, you can monitor the progress via console output or using TensorBoard if integrated. Key metrics to watch include:
•	Loss: Indicates how well the model is learning.
•	mAP (mean Average Precision):Measures the accuracy of the model.
•	Precision and Recall: Provide insights into the model's performance.
Annotation Formats:
LabelImg can save annotations in several formats, but for YOLOv8, you should use the YOLO format:

YOLO Format: Each annotation file (per image) contains lines with the format:
  
  <object-class> <x_center> <y_center> <width> <height>
  
  Where `x_center`, `y_center`, `width`, and `height` are normalized values between 0 and 1.

Disclaimer:

This project involves setting up and training machine learning models, which can be resource-intensive and time-consuming. Users should ensure they have the necessary computational resources and expertise to follow through the entire process. Additionally, real-time object tracking may have limitations based on the complexity of the scene and the capabilities of the chosen tracking algorithm. The accuracy of the tracking system depends significantly on the quality and diversity of the training data. Users must also adhere to ethical guidelines and obtain necessary permissions if tracking involves recording individuals or sensitive content.
