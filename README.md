# Few-Shot-X-Ray-classification

## Overview
Welcome to the Few-Shot X-ray Image Classification project! This project aims to develop a high-performance classifier for X-ray images using few-shot learning techniques. With an F1 score exceeding 90%, it stands out as a winner in EY's data science competition.

## Purpose
The goal is to create an efficient and interpretable model for classifying X-ray images, leveraging few-shot learning to overcome the challenge of limited annotated medical data.

## Project Structure
### Data Used
X-ray images downloaded from kaggle.
### Project execution schema
![image](https://github.com/user-attachments/assets/9988323d-3e6d-4fd2-9cc0-d7ccb86b2fcc)
After basic image resizing and normalization, a small part of the training dataset (1% to 10% of the available train data) is passed into the pre-trained visual classifier (in this case DenseNet161) with the last layer removed. The extracted features are used as input to train an SVC (Support Vector Classifier) model, which learns to distinguish between anomalous cases of pneumonia on X-ray images and normal, healthy images.

### Benefits of this solution
- **Low Training Data Requirement**: This solution repeatedly achieves close to 90% F1 score with as few as 10 images of both healthy and anomalous lung images. This is incredibly beneficial in medical imaging scenarios where well-annotated data is hard to come by.

- **Low Computational Needs**: Since only the SVC classifier is trained and not the neural network itself, the computational requirements are minimal. This simplifies the usage and implementation of this solution by third parties.

- **Great Interpretability**: Thanks to the usage of Grad-CAM and the inherently higher interpretability of SVC over most neural network-based solutions. This is also helpful for gaining regulatory approval, which is especially useful in the medical field.

## Performance characteristics
- **High Accuracy**: Over 90% F1 score.
- **Data Efficiency**: Operates effectively with 10%-1% of the dataset (100 to 10 images per class).
- **Resource Efficiency**: Requires minimal computational power.
- **Scalable**: Adaptable to other medical images.
- **Deployable**: Ready for real-world use.

## Possible Future Directions
Data Augmentation: Explore advanced techniques to enhance performance.
Ensemble Methods: Combine models for improved accuracy.
Real-Time Deployment: Implement in diagnostic systems.
Broader Applications: Extend to other medical imaging tasks.

## Usage
To use this project:

Simply clone or download the .ipynb file and run the provided code inside.

## Note

There is a powerpoint presentation in this repositiory which goes a bit deeper into the proposed solution.

## Contact
For inquiries, please contact krzy.miler@gmail.com.
