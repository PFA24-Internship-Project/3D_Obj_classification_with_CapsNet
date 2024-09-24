
#  3D Object Classification Using Capsule Networks
 ## Project Overview
This project explores the capacity of **Capsule Networks (CapsNet)** to classify aneurysms and vessel conditions from 3D medical data. The aim is to assess how well CapsNet captures spatial hierarchies and complex structures in medical imaging, offering potentially better performance compared to traditional CNNs for these specific tasks.

## Table of Contents
- [Project Overview](#project-overview)
- [Motivation](#motivation)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Model Architecture](#modelArchitecture)
- [Installation](#installation)
- [Results](#results)
- [Authors](#authors)
- [Acknowledgements](#acknowledgements)
## Motivation

The detection and classification of aneurysms and vessel abnormalities are critical tasks in medical diagnostics. Traditional Convolutional Neural Networks (CNNs), while powerful, often struggle with capturing the intricate spatial relationships in 3D medical images, which can lead to misclassification or missed details. **Capsule Networks (CapsNet)**, with their ability to preserve spatial hierarchies and understand complex object orientations, offer a promising alternative. 

Our motivation is to leverage this unique capability of CapsNet to enhance the accuracy and reliability of aneurysm and vessel classification. By improving the precision of these classifications, we aim to contribute to more effective diagnostic tools that can assist medical professionals in identifying life-threatening conditions earlier and more accurately.

## Dataset: IntrA - 3D Intracranial Aneurysm Dataset

The IntrA dataset is an open-access collection designed for deep learning applications in medical diagnostics. It provides 3D models of intracranial aneurysm segments, with detailed segmentation annotations. This dataset is essential for tasks like the classification and segmentation of aneurysms, which are critical for diagnosing and treating intracranial aneurysms. 

IntrA includes:
- **103 complete 3D models** of brain vessels reconstructed from 2D MRA scans.
- **1909 blood vessel segments**, including 215 aneurysm segments for classification tasks.
- **116 manually annotated aneurysm segments**, aimed at improving segmentation models used in preoperative planning, such as identifying the neck of an aneurysm for clipping operations.

This dataset offers opportunities for exploring point-based and mesh-based deep learning models in medical image analysis, promoting the accurate diagnosis and surgical planning for intracranial aneurysms.

[Dataset Link](https://github.com/intra3d2019/IntrA/blob/master/README.md)

## Methodology
We utilized the IntrA dataset with 3D models of intracranial aneurysms, converting them into voxels for efficient processing. A hybrid VGG-CapsNet model was employed, combining VGG’s feature extraction with CapsNet’s dynamic routing to classify aneurysm conditions.

The trained model was then deployed in an application to provide real-time classification, aiding medical professionals in clinical decision-making.

## Model Architecture
The project uses a hybrid model combining VGG for feature extraction and CapsNet for dynamic routing and handling spatial relationships. Key components include:

Voxel-based input for efficient processing of 3D models
VGG layers for extracting relevant features from the input data
CapsNet with dynamic routing to capture spatial hierarchies and relationships.

## Installation
To set up this project locally, follow these steps:

### 1.Prerequisites
Python 3.8+ is required to run the application.
Ensure that you have pip installed to handle dependencies.
Steps
### 2.Clone the repository:
git clone https://github.com/PFA24-Internship-Project/3D_Obj_classification_with_CapsNet

### 3.Install the required dependencies:
pip install -r requirements.txt

### 4.Prepare the model weights:
Make sure to  install  the model weights (weights-47.weights.h5)  from [link](https://drive.google.com/drive/folders/1u9EOpJ6-FmmAHKbMYMqR_gtGmcFWhLxB?usp=drive_link) and verify that  is in the correct path (Model/ directory). 


### 5.Set up the Streamlit configuration:
Check the .streamlit/config.toml file for any necessary changes regarding the Streamlit server configuration.

### 6.Run the application:
streamlit run code/APP_Web/Accueil.py

## Results
- **Vessel %**: [95%]  
- **Aneurysm %**: [93%]   
- **F1-Score**: [94%]

**Authors:**  
- Olaia Mechal  
- Souhaila El Kadaoui  
-  Hamza Kholti 
- Khadija Elabbioui 

## Acknowledgements

This project was supported by **3D Smart Factory Society**, whose resources and expertise have significantly contributed to the successful completion of this work. We extend my sincere gratitude for their invaluable support.





