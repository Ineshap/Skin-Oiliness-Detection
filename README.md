# Skin Oiliness Detection

This project consists of two main components: a model for skin oiliness severity detection and an API for real-time inference using the trained model.

## Model Training

### Requirements
- Python 3.x
- TensorFlow 2.x
- OpenCV
- Flask
- Matplotlib

### Setup
1. Install the required Python packages using `pip install -r requirements.txt`.
2. Organize your dataset into training, validation, and test sets. Ensure that each class of images is placed in separate folders.
3. Update the paths to your training, validation, and test data in the `train_path`, `valid_path`, and `test_path` variables in the training script (`train_model.py`).
4. Run the training script: `python train_model.py`. This script loads the pre-trained VGG16 model, adds custom layers on top, compiles the model, and trains it on the provided dataset.

### Model Saving
After training, the model will be saved as `Skin_Oiliness_Severity_Detection_Final_Inesha_12-30.h5`.

## API for Real-Time Inference

### Requirements
- Python 3.x
- TensorFlow 2.x
- Flask
- OpenCV

### Setup
1. Install the required Python packages using `pip install -r requirements.txt`.
2. Place the trained model file (`Skin_Oiliness_Severity_Detection_Final_Inesha_12-30.h5`) in the same directory as the API script (`app.py`).
3. Run the API script: `python app.py`. This script initializes a Flask web application and exposes an endpoint for uploading images or capturing images from a webcam. It uses the trained model to predict the oiliness severity of the skin in the uploaded images.

### API Usage
- Visit `http://localhost:5001/` in your web browser to access the web interface for uploading images or capturing images from a webcam.
- Choose the source of the image (device or webcam) and upload an image or capture an image.
- The API will return the predicted skin oiliness severity level (Oily Skin, Normal Skin, or Dry Skin) based on the uploaded/captured image.

