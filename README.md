# Deep Learning Crowd Counting

## Project Description
This project focuses on implementing deep learning models for crowd counting. It involves building, training, and evaluating multiple CNN-based architectures that estimate the number of people in images by generating and analyzing density maps.

---

## Objective
- Prepare image data and annotations for density map generation.  
- Develop several crowd counting models using CNN architectures.  
- Evaluate model performance using MSE and GAME metrics.  
- Visualize predicted versus ground truth density maps.  
- Save trained models for future inference.

---

## Dataset Information
- Dataset includes images with annotated points representing individual people.  
- Each annotation is converted into a density map using a Gaussian kernel.  
- The dataset is split into training and testing subsets for model evaluation.  
- All images are preprocessed and resized to ensure consistency across the dataset.

---

## Methodology

### 1. Data Preparation and EDA
- Loaded images and annotation files.  
- Used a custom `get_coords` function to convert coordinate strings into numerical arrays.  
- Visualized sample images with annotation points for verification.  
- Generated density maps using Gaussian kernels to represent crowd distributions.  

### 2. Model Development
Implemented and trained multiple architectures:
- **CSRNet (VGG-based)** with a decoder for density estimation.  
- **MCNN (Multi-Column CNN)** for handling different crowd densities and scales.  
- **ResNet101-based** model for feature extraction and improved accuracy.  

### 3. Evaluation
- Models were evaluated using **Mean Squared Error (MSE)** and **Grid Average Mean absolute Error (GAME)** metrics.  
- Visualization compared predicted density maps with ground truth to assess model performance visually.

### 4. Model Saving
- Trained models were saved for reuse in inference and deployment.

---

## Results and Findings
- CSRNet achieved stable predictions with accurate density estimations.  
- MCNN showed strong adaptability across varied crowd densities.  
- ResNet101-based model provided improved generalization due to deeper feature extraction.  
- Visual comparisons confirmed the models' ability to capture realistic crowd patterns.

---

## Conclusion
This project demonstrates how convolutional neural networks can effectively estimate crowd density from images. Through different architectures like CSRNet, MCNN, and ResNet-based models, it shows that deep learning can deliver reliable and scalable solutions for real-world crowd counting tasks.
