# MudraLingua - Indian Sign Language Tutor

MudraLingua is a web-based application designed to help users learn and visualize **Indian Sign Language (ISL)** using machine learning techniques. The project leverages **computer vision and deep learning** to recognize hand gestures and translate them into corresponding text, facilitating communication for individuals with speech or hearing impairments.

## Features
- Real-time hand gesture recognition using a trained machine learning model.
- Support for **10 different hand signs** based on a custom dataset.
- Interactive web-based interface for easy learning.
- Multiple approaches explored for gesture recognition.

## Technologies Used
- **Python**
- **TensorFlow** for deep learning-based sign recognition.
- **OpenCV** for real-time hand tracking and image preprocessing.
- **MediaPipe** for an alternative gesture recognition approach.
- **JavaScript, HTML, CSS** for frontend development.
- **Flask** (or Node.js) for backend server handling (if applicable).

## Training the Machine Learning Model

### Dataset Preparation
Since there was no standard dataset available for **Indian Sign Language (ISL)**, I trained the model using a **custom dataset**. The dataset was created by:
1. **Capturing hand gesture images** using OpenCV from multiple angles and lighting conditions.
2. **Augmenting data** to improve model robustness (e.g., rotation, scaling, flipping, brightness adjustments).
3. **Labeling** the images manually to map each gesture to its corresponding sign.

### Model Training with TensorFlow
Once the dataset was prepared, I trained a **Convolutional Neural Network (CNN)** model using TensorFlow:
- Used **TensorFlow and Keras** for model implementation.
- Implemented **data augmentation** techniques to generalize the model better.
- Optimized using **Adam optimizer** and categorical cross-entropy loss.
- Achieved a reasonable **accuracy after multiple training iterations**.

## Alternate Approaches Explored
To ensure robustness and efficiency, I experimented with **alternative methods** for gesture recognition:

### 1. MediaPipe Gesture Recognition Model
- **Google’s MediaPipe framework** provides a pre-trained hand-tracking model.
- Extracts **21 key landmarks** from the hand, making gesture classification efficient.
- Used these **landmark coordinates** as feature vectors to classify hand signs using an ML model.
- Faster inference time due to **lightweight nature** of MediaPipe.

### 2. OpenCV-Based Approach + Custom Classification Model
- Extracted **hand contours and keypoints** using OpenCV.
- Used **Convex Hull and Finger Counting** methods to analyze hand shape.
- Trained a **custom classification model** on the extracted hand coordinate data.
- Although this method was computationally cheaper, it lacked the accuracy of deep learning models.

## Challenges and Learnings
- **Building a dataset from scratch** was challenging but helped improve data quality.
- **Balancing model accuracy and inference speed** was crucial for real-time performance.
- **Comparing different recognition approaches** provided insights into the best trade-offs between speed and accuracy.

## Future Enhancements
- Expanding the dataset to include **more gestures and signs**.
- Optimizing the TensorFlow model for **mobile deployment**.
- Enhancing the UI/UX for a better learning experience.
- Exploring **transformer-based models** for improved recognition.

## How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/SatyajitGarud/MudraLingua.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the application:
   ```bash
   python app.py
   ```

## Acknowledgments
Special thanks to the **open-source community** and **TensorFlow/MediaPipe teams** for providing powerful tools that made this project possible.

## Author
**Satyajit Garud**  
[GitHub](https://github.com/SatyajitGarud) | [LinkedIn](https://www.linkedin.com/in/satyajit-garud-099306262/)
