
# License Plate Recognition using YOLOv8 and EasyOCR

## Overview 
This project implements an automated license plate recognition (ALPR) system using YOLOv8 for license plate detection and EasyOCR for text extraction. The system is capable of detecting license plates in images and recognizing the characters on them with high accuracy.

## Project Workflow 
Train YOLOv8 for License Plate Detection – A custom YOLOv8 model is trained on a labeled dataset of license plates. Run Inference on Test Images – The trained model is used to detect license plates in new images. Extract the Most Confident Bounding Box – The detection with the highest confidence score is selected. Apply OCR for Text Recognition – The detected license plate region is passed to EasyOCR to extract the alphanumeric characters. Display Results – The image is displayed with bounding boxes and recognized text.

## Dataset
The model is trained using a custom dataset that includes 923 annotated images of license plates which was downloaded from roboflow. The dataset is defined in a YOLO format YAML file, specifying training and validation image directories.

### Dataset link: 
https://universe.roboflow.com/janet-rini-eaojj/license-plate-detection-tdv0k

## Requirements 
Python 3.8+ 
Ultralytics (YOLOv8) 
OpenCV 
EasyOCR 
Google Colab (optional, for training)

## Implementation Details
### YOLOv8 Model Training: 
The model is trained for 40 epochs with an image size of 640x640 to improve detection accuracy. Bounding Box Selection: Among multiple detections, only the one with the highest confidence score is used for OCR processing. Text Recognition: EasyOCR is applied to extract the license plate number from the detected region.

## Results
The YOLOv8 model achieves high accuracy in detecting license plates across different lighting conditions and angles. EasyOCR provides reliable character recognition, though performance may vary depending on image clarity.
### Precison : 0.9189994245241669
### Recall : 0.8883495145631068

## Conclusion
This project demonstrates an effective approach to license plate recognition by combining deep learning-based object detection with OCR technology. It can be further optimized for real-world applications such as automated parking systems, traffic monitoring, and law enforcement.
