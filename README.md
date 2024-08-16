# Vehicle Speed Estimation Project
## Project Overview
This machine learning project utilizes YOLOv8 to detect and track vehicles in video frames, trained on a meticulously annotated custom dataset. The system incorporates speed estimation by defining a Region of Interest (ROI) within each frame. Utilizing OpenCV, the ROI enables precise speed calculations based on vehicle displacement over time. The outcome is a powerful combination of vehicle identification, tracking, and real-time speed estimation, applicable for traffic monitoring and law enforcement tasks.

## Requirement
1. Python 3.8.10
2. Ultralytics  8.0.183
3. Pandas 2.0.3
4. NumPy 1.23.0
5. Cv2  4.8.0

## Data Preparation

The data preparation stage of the machine learning project is where we lay the foundation for successful model training. This crucial step involves gathering, cleaning, and organizing the raw data, transforming it into a structured and meaningful format that can be readily utilized for model training.

### Execution Instructions

To initiate the data preparation process,execute the provided "get_annotaions.ipynb" script by running all its cells.
Ensure you have the necessary dependencies installed, as listed in the project's requirements. Adjust any configuration parameters within the script to suit your system and project requirements.

```
python get_annotaions.ipynb
```

### Functionality Overview

The data preparation script performs a series of essential tasks, including data cleaning, handling missing values, addressing outliers, and organizing the dataset into a format suitable for machine learning model training. It implements various preprocessing techniques to enhance the quality and relevance of the data, paving the way for more effective model learning.

### Expected results

Upon successful execution, you can anticipate a well-prepared dataset stored in the specified output directory. 
The resultant prepared data should be precisely in the below-mentioned format.
```
train/	|-- images/
		|   |-- 1.jpg
		|   |-- 2.jpg
		|   |-- ...
	|-- labels/
		|   |-- 1.jpg
		|   |-- 2.jpg
		|   |-- ...
		|
val/	|-- images/
		|   |-- 1.jpg
		|   |-- 2.jpg
		|   |-- ...
	|-- labels/
		|   |-- 1.jpg
		|   |-- 2.jpg
		|   |-- ...
		|
test/	|-- images/
		|   |-- 1.jpg
		|   |-- 2.jpg
		|   |-- ...
```

## Model training

 The model training phase of the machine learning project is a pivotal step where we harness the power of our carefully prepared data to train a robust and effective model. This section provides comprehensive guidance on running the model training script, insight into its functionalities, and an overview of the expected results.
 
#### Example output of the model training:
 ![image](https://github.com/user-attachments/assets/1c14e47b-cc6c-4831-9d41-d55243b0e6f7)

#### Training results:
![image](https://github.com/user-attachments/assets/a7d57c78-a1e1-4662-8395-83d14173de94)

![image](https://github.com/user-attachments/assets/24bd19f3-7a20-41c1-8542-157f1fdb2298)

![image](https://github.com/user-attachments/assets/abc45a09-324d-4e0f-932d-0645b70b882c)

### Execution Instructions

Initiating the model training script is straightforward. Download all the files in the "model_taining folder" and execute the provided "model_training.ipynb" script by running all its cells. 
```
python model_training.ipynb
```
Before running the script, ensure all required dependencies are installed as specified in the project documentation. Customize any configuration parameters within the script to align with your project objectives.

### Functionality Overview

The model training script orchestrates an iterative learning process over the prepared dataset. It will be trained to detect vehicles like cars and vans, guiding the machine-learning model through multiple epochs to refine its parameters. Notably, the training process is configured to run for ten epochs, each representing a complete pass through the dataset. Additionally, a specific image size (imgsz) of 244 pixels is employed, contributing to the model's ability to extract meaningful features from the input data.

### Expected results

Upon successful execution, expect the script to produce a trained weights file(found in a folder named runs) ready for deployment. The model will learn from the input data, capturing essential features and relationships and enabling it to make predictions based on new, unseen data. The expected results include model performance metrics, such as accuracy and loss, providing insights into the effectiveness of the trained model. These outcomes are critical for evaluating the model's capability to generalize to real-world scenarios and make accurate predictions.

## Speed Calculation

Welcome to the speed estimation phase of our machine learning project, where the culmination of meticulously trained models and well-prepared datasets takes center stage. This section provides comprehensive guidance on running the speed estimation script, delving into its functionalities, and offering insights into the expected results.

### Execution Instructions

Running the speed estimation script is a straightforward procedure. Download all the files in the "speed_calculation folder" and execute the provided "Speed_Estimation.ipynb" script by executing all its cells. 
```
python Speed_Estimation.ipynb
```
Before running the script, ensure that all necessary dependencies are installed, as outlined in the project documentation. Additionally, ensure the trained model file is available for accurate speed predictions.

### Functionality Overview

The speed estimation script harnesses the power of computer vision, utilizing OpenCV (cv2) alongside the pre-trained machine learning model. It performs object detection and tracking on video frames, defining a specific Region of Interest (ROI) where vehicle speed is to be measured. By precisely calculating the displacement of vehicles within the ROI over time, the script accurately finds the speed of each passing vehicle. This integration of object detection, tracking, and speed estimation enhances the model's utility in real-world scenarios.

### Expected Results

Upon successful execution, expect a comprehensive output. The script generates a full-fledged video showcasing the seamless detection of objects and the simultaneous display of their respective speeds. A text file is also produced detailing the speed information for each identified vehicle. This holistic approach to speed estimation provides visual insights and creates a structured data output for further analysis and application in diverse domains such as traffic monitoring and law enforcement.

## Results

In conclusion, the culmination of our efforts in this machine learning project yields compelling results. The trained model, honed through meticulous data preparation and model training phases, showcases a remarkable ability to detect cars and vans accurately. The model seamlessly integrates object detection with speed estimation when applied to video data, providing a visually informative output. The generated video dynamically displays the speed of various vehicles, offering a tangible representation of the model's real-world applicability. Simultaneously, the accompanying text file furnishes comprehensive speed details for each detected vehicle, facilitating further analysis and insights. These outcomes collectively underscore the efficacy of our machine learning approach in addressing complex tasks such as vehicle detection and speed estimation, making it a valuable asset in diverse applications ranging from traffic management to public safety.
