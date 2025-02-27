# YOLO Car License Plate Detection

This notebook implements a car license plate detection system using YOLOv8. The system is designed to detect and localize license plates in images of vehicles using a custom-trained YOLO model.

## Setup and Dependencies

The notebook requires the following main dependencies:
- OpenCV (cv2)
- Pandas
- XML ElementTree
- Ultralytics YOLO
- Google Colab (for GPU acceleration)

## Project Structure

The project consists of several key steps:

1. **Data Preparation**
   - Mounting Google Drive for data access
   - Downloading and extracting car image datasets
   - Converting XML annotations to CSV format
   - Processing image dimensions and coordinates

2. **Data Processing**
   - XML to CSV conversion for annotations
   - Image dimension extraction
   - Coordinate normalization for YOLO format
   - Dataset organization for training

3. **Model Training**
   - Using YOLOv8 small model (yolo11s)
   - Training configuration:
     - 50 epochs
     - Batch size: 32
     - Image size: 640x640
     - AdamW optimizer
     - Cosine learning rate scheduling
     - Initial learning rate: 0.001

## Key Features

- Handles Persian/Farsi annotations for license plates
- Processes both training and validation datasets
- Includes data preprocessing for YOLO format
- Implements custom data loading and transformation
- Uses modern YOLO architecture for accurate detection

## Model Performance

The trained model achieves:
- mAP50: 0.98 (98%)
- mAP50-95: 0.793 (79.3%)
- High precision and recall on license plate detection

## Usage

1. Mount Google Drive and set up the environment
2. Prepare your dataset in the correct format
3. Run the data preprocessing cells
4. Execute model training
5. Use the trained model for inference on new images

## Dataset Structure

The dataset includes:
- Training images with corresponding XML annotations
- Validation set for model evaluation
- Annotations containing license plate coordinates

## Notes

- The model is specifically trained for license plate detection
- Uses YOLO format for object detection
- Includes data augmentation for better generalization
- Implements proper train/validation split
