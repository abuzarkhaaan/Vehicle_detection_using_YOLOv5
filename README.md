
# Vehicle Detection for Pakistani Traffic Using YOLOv5X

This repository contains a YOLOv5X model trained specifically for vehicle detection in Pakistani traffic. The model is capable of detecting various types of vehicles common in Pakistan, including **chingqi**, **rikshaw**, **bicycle**, **bus**, **motorcycle**, **car**, **heavy transport vehicles (HTV)**, and **ambulance**. The model was trained using a custom dataset to handle the unique challenges of Pakistani traffic conditions such as congested roads, diverse vehicle types, and complex environments.

## Key Features:
- **Multi-Class Vehicle Detection**: Capable of detecting 8 different types of vehicles common on Pakistani roads.
- **High Accuracy**: Trained using YOLOv5X, which provides accurate real-time detection with minimal computational requirements.
- **Custom Dataset**: Dataset specifically curated to include vehicles and traffic conditions unique to Pakistan.

## Detected Vehicle Classes:
- **Chingqi** (Three-Wheeler)
- **Rikshaw** (Auto Rickshaw)
- **Bicycle**
- **Bus**
- **Motorcycle**
- **Car**
- **HTV** (Heavy Transport Vehicle)
- **Ambulance**

## Model Architecture:
The model is based on **YOLOv5X**, the largest variant of the YOLOv5 family, known for its capability to detect small objects with higher accuracy, which is essential for distinguishing between similar vehicle types such as chingqi and rikshaw.

## Dataset:
The dataset consists of images taken from real-world traffic conditions in various cities across Pakistan. It includes scenarios such as:
- **Dense traffic** during rush hours
- **Various lighting conditions** (daytime, nighttime, and overcast)
- **Urban and rural environments** 
- **Vehicles in motion** and **parked vehicles**

The dataset was manually labeled and contains thousands of instances for each vehicle type.

## Usage:

### 1. Clone the Repository:
```bash
git clone https://github.com/abuzarkhaaan/vehicle-detection-yolov5X.git
cd vehicle-detection-yolov5X
2. Install Dependencies:
Make sure to install the required dependencies before running the model:


pip install -r requirements.txt
3. Inference:
To run inference on images or videos, use the following command:


python detect.py --weights yolov5x.pt --source your_image_or_video_path --img-size 640 --conf 0.5
Where:

--weights is the path to the trained model weights.
--source is the path to the image or video file.
--img-size specifies the size of the input images.
--conf sets the confidence threshold for detection.
4. Training:
To retrain or fine-tune the model on your custom dataset, run:


python train.py --img 640 --batch 256 --epochs 10000--data_data.yaml --weights yolov5x.pt
5. Evaluate Model Performance:
Evaluate the model's performance using the validation dataset:


python val.py --weights yolov5x.pt --data data.yaml
6. Export Model:
Export the trained model for deployment in various formats (ONNX, CoreML, TensorRT, etc.):


python export.py --weights yolov5x.pt --img 640 --batch 1 --device 0
Performance Metrics:
The model was evaluated on a custom validation dataset with the following results:

Precision: 0.85
Recall: 0.78
mAP@50: 0.81
Inference Speed: ~20ms per image (on NVIDIA RTX 3080)
Future Improvements:
Additional Vehicle Classes: Expand the model to detect more specific vehicle types such as tractors, vans, and luxury cars.
Optimization for Edge Devices: Improve model efficiency for use on mobile and embedded devices for real-time traffic monitoring.
Integration with Traffic Management Systems: Use this model to assist in automated traffic management and law enforcement.
Acknowledgements:
YOLOv5 by Ultralytics for the base architecture.
Open-source datasets and contributors for providing valuable training data.
License:
This project is licensed under the MIT License. See the LICENSE file for details.

Contact:
For any inquiries or support, feel free to contact:

Name: Abuzarkhaan
Email: abuzarkhaaan580@gmail.com

