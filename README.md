# Access_Control_Face-Mask_Detector
In the wake of the worldwide COVID-19 pandemic, ensuring safety measures such as wearing face masks has become essential. The Access Controlled Face Mask Detector project aims to detect the presence of face masks on human faces in real-time live streaming video. This project combines deep learning, image processing, and hardware components to create an intelligent system that enforces mask-wearing compliance.

Introduction: In the current pandemic scenario, the Access Controlled Face Mask Detector project addresses the need for effective protection mechanisms. The primary objective of this project is to detect whether individuals are wearing face masks or not. Utilizing the Convolutional Neural Network (CNN) architecture's MobileNet V2 deep learning algorithm, this is possible. The system interfaces with an Arduino module and a servo motor to control access to public spaces based on mask detection results.

Architecture: The project architecture involves several components:

MobileNet V2 Algorithm: A deep learning image classification algorithm that assigns weights to objects in images and differentiates between them

Arduino Module: Interfaces with the mask detection model and controls the servo motor responsible for granting access.

Servo Motor: An automatic sensor door that opens or remains closed based on the mask detection results.

Camera Interface: Utilizes OpenCV for capturing real-time video streams and detecting faces.

Dataset: Contains masked and unmasked face images for training the model.

Image Data Generator: Augments the dataset by applying transformations to improve model performance.

PY Serial: Connects the software part to the hardware part, enabling communication between Python code and the Arduino module.

Dataset: The project employs a dataset consisting of masked and unmasked face images. Initially, the dataset underwent preprocessing to remove duplicates and noise. Cleaning was done to enhance the accuracy of the model. The dataset was divided into masked and unmasked images and subjected to noise removal, duplicate removal, and error correction.

Model Building: The mask detection model is built using the MobileNet V2 algorithm, which assigns importance to objects in images. The architecture involves a base model and a head model. The base model uses the MobileNet V2 algorithm's pre-trained weights for image classification. Max-pooling and fully connected layers are added to enhance accuracy.

Model Training: The model is trained using an Adam optimizer with binary cross-entropy loss. Image Data Generator augments the dataset, improving model performance. The model's accuracy, precision, recall, and F1 score are evaluated using a confusion matrix.

Interfacing Camera: The system interfaces with a camera using OpenCV for real-time video streaming. The face detection model identifies faces, and the mask detection model assesses whether individuals are wearing masks. Rectangular boxes and labels are displayed around faces in the video stream.

Interfacing Hardware Components: The project interfaces with hardware components using PY Serial and an Arduino module. The Arduino controls a servo motor that acts as an access sensor. Access is granted by rotating the servo motor only when a person wearing a mask is detected.
This machine learning project was built during COVID to ensure the safety of public
