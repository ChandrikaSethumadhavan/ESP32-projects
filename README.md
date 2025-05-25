# ESP32-projects

Device used : ESP32-CAM / AI thinker ESP32 board

Platforms used : Edge impulse.com

## Exploring ESP32-CAM's functionality with Edge impulse platform ##

What is an ESP32 anyway?

What Is Object Detection?
Combination of:

* Image Classification: Identifies what is in the image.

* Image Localization: Determines where the object is (usually with bounding boxes).

Once trained, the system can detect objects in real-time and return their location in an image.

Why this combination?


* Object detection? Easy, like teaching a child about Apples vs Oranges.

* Object detection in setups with humongous GPUs? Basic

* Object detection in a small module that consumes power in mWs? Mind blowing! 

The new future is running high end ML / NNs models on energy efficient devices. Thus the concept of TinyML was born.











## Introduction to Edge Impulse Workflow ##

Collect Images – Using a webcam, ESP32-CAM, or smartphone.In our case, ESP32 CAM

Label Images – Assign bounding boxes and labels.

Train Model – Build a neural network model to recognize objects.

Export Model – As Arduino library or firmware for ESP32.

Deploy & Test – Upload to ESP32 and detect objects in real-time. This can be seen on the arduino IDE serial monitor.




## Model Training - Impulse Design Settings ##

Image resolution: 96x96 or 48x48 (48 recommended for ESP32)

Grayscale images for reduced processing load

Model: MobileNet v2 0.1 (suitable for ESP32)


## Model Deployment ##

Exported model as an Arduino ZIP library

Loaded into Arduino IDE and uploaded to the ESP32.

Used built-in example sketch for ESP32-CAM object detection.

Displays object class and bounding box coordinates via Serial Monitor.



##  Live Testing and observations ##

The ESP32 successfully identified:

* Individual objects

* Multiple objects simultaneously

* Confidence varied based on object angle and camera quality.


