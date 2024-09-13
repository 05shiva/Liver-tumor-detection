Liver Tumor Detection
This project is a web-based application for detecting liver tumors from MRI images. It uses a machine learning model to predict the presence of a tumor based on the uploaded images. The model is deployed using Flask and Docker.

Table of Contents
Project Overview
Features
Requirements
Setup and Installation
Usage
Docker Deployment
File Structure
Contributing
License
Project Overview
The Liver Tumor Detection system allows users to upload MRI images through a web interface. It processes the image and predicts whether a tumor is present using a pre-trained deep learning model (liver_tumor_detection_mod.h5). The application is deployed within a Docker environment, ensuring portability and ease of use.

Features
Upload MRI images through a simple web interface.
Predicts the presence of a liver tumor based on the uploaded image.
Uses a deep learning model (liver_tumor_detection_mod.h5) trained for high accuracy.
Deployed using Docker for consistent and scalable deployment.
Interactive web interface with real-time predictions.
Requirements
Python 3.8+
Docker
Flask
TensorFlow or Keras for loading the .h5 model
OpenCV for image processing
For specific dependencies, refer to requirements.txt.

Setup and Installation
1. Clone the repository
bash
Copy code
git clone https://github.com/05shiva/Liver-tumor-detection
cd Liver-tumor-detection
2. Install dependencies
To install the required Python packages, run:

bash
Copy code
pip install -r requirements.txt
3. Running the Application
To run the Flask app locally:

bash
Copy code
python app.py
The app will be accessible at http://127.0.0.1:5000/.

Docker Deployment
To deploy the application using Docker, follow these steps:

1. Build the Docker image
bash
Copy code
docker build -t liver-tumor-detection .
2. Run the Docker container
bash
Copy code
docker run -d -p 5000:5000 liver-tumor-detection
The application will be available at http://localhost:5000/.

File Structure
php
Copy code
├── Dockerfile                 # Docker configuration
├── app.py                     # Main Flask application
├── liver_tumor_detection_mod.h5 # Pre-trained model for tumor detection
├── model.py                   # Model loading and prediction logic
├── requirements.txt           # List of dependencies
├── templates/
│   └── index.html             # Frontend HTML page
├── static/
│   └── [Static assets like CSS, JS, etc.]
├── uploads/                   # Directory for uploaded images
│   └── [Uploaded images for prediction]
├── mini2/
├── img1.jpg, img2.jpg, ...     # Sample MRI images
├── Screenshot_2024-06-15_203652.png # Screenshot examples
Usage
Upload an MRI image using the web interface.
Click the "Predict" button.
The system will display the result, indicating whether a tumor is detected.
Contributing
Contributions are welcome! Feel free to open issues or submit pull requests to improve the application.
