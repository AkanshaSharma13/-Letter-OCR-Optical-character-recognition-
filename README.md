# Letter-OCR: Optical Character Recognition

## Problem Statement
Develop an efficient and accurate system for recognizing English letters.

## Introduction
The objective of the letter recognition task is to classify a large number of black-and-white rectangular pixel displays into one of the 26 capital letters of the English alphabet.

## Motivation
The motivation behind building a letter OCR project is to create a system that can understand and interpret handwritten or printed letters, similar to human capabilities. This project has numerous practical applications, including:

- Automating tasks like sorting mail
- Digitizing documents
- Assisting individuals with disabilities who may have difficulty reading printed text

By utilizing machine learning techniques, we aim to train a computer program to recognize and classify letters accurately from images or scanned documents, making letter recognition faster, more efficient, and accessible to everyone.

## Dataset
The dataset is sourced from the UCI ML repository and consists of images of English alphabets in 20 different fonts. Each letter is presented within a bounding box containing black and white pixels with varying intensity. 

- **Task:** Classification
- **Objective:** Classify pixel displays into one of the 26 capital letters of the English alphabet.
- **Data Characteristics:**
  - **Fonts:** 20 different styles
  - **Variations:** Random distortions applied to each letter, resulting in 20,000 unique stimuli
  - **Attributes:** 16 primitive numerical attributes, including statistical moments and edge counts
  - **Data Range:** Attributes scaled to integer values from 0 to 15

## Features
Each character image is converted into 16 primitive numerical attributes, which include:

- **Statistical Moments:** Metrics like mean and variance, providing information about the distribution of pixel intensities.
- **Edge Counts:** Information about the number of edges or transitions between different pixel intensities, indicating the presence of edges or contours.

## Data Preprocessing

### Data Cleaning
- **Missing Values:** No missing values are present in the dataset.

### Data Transformation
- **Conversion into Numerical Attributes:** Character images are represented using 16 numerical attributes.

### Feature Selection/Extraction
- **Feature Extraction:** Statistical moments and edge counts are extracted from the images to represent the letters.

### Data Integration
- No specific data integration process is applied.

### Normalization
- **Scaling Attributes:** The attributes are scaled to fit within the range of 0 to 15, simplifying feature representation and reducing computational complexity.

### Encoding Categorical Variables
- The target variable, representing the capital letter, is encoded numerically.

### Handling Imbalanced Data
- No explicit mention of handling imbalanced data. If necessary, techniques like resampling or specific evaluation metrics can be applied.

### Data Partitioning
- The dataset is divided into training (16,000 samples) and testing (4,000 samples) subsets to assess the model's performance on unseen data.

## Techniques for Image Enhancement, Noise Reduction, and Normalization

### Image Enhancement
- **Histogram Equalization:** Improves contrast by redistributing pixel intensities.
- **Adaptive Histogram Equalization:** Enhances local contrast for varying lighting conditions.
- **Gamma Correction:** Adjusts brightness and contrast using a power-law transformation.

### Noise Reduction
- **Gaussian Blur:** Smooths out noise and reduces detail.
- **Median Filtering:** Removes salt-and-pepper noise by replacing each pixel's value with the median of neighboring pixels.
- **Bilateral Filtering:** Reduces noise while preserving edges.

## Acknowledgments
- UCI Machine Learning Repository for providing the dataset.
