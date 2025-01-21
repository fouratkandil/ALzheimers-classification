Classification of Alzheimer’s Cases Using CNNs

Overview
This project focuses on classifying Alzheimer's disease cases using Convolutional Neural Networks (CNNs). Two experiments were conducted:
1. Classification with four categories: Mild Demented, Moderate Demented, Non-Demented, and Very Mild Demented.
2. Classification with three categories: Alzheimer's Disease (AD), Mild Cognitive Impairment (MCI), and Cognitively Normal (CN).

Additionally, pretrained models (Residual Net, Efficient Net, and Mobile Net) were evaluated for performance comparison.



Features
- Custom CNN Model: Developed from scratch for image classification.
- Pretrained Models: Fine-tuned models for comparison.
- Streamlit Interface: User-friendly tool for real-time image classification.



 Datasets
- Four-Class Dataset: 5,154 images distributed among the four categories.
- Three-Class Dataset: Images restructured into three broader categories.

 Data Preprocessing
- Resized images to 128x128 pixels.
- Normalized pixel values to [0, 1].
- Applied one-hot encoding for labels.
- Training/Test split: 80% training, 20% testing.

 Data Augmentation
To improve generalization, the following techniques were applied:
- Rotation (up to 40 degrees)
- Width and height shifts (up to 30%)
- Shearing, Zooming (up to 30%)
- Horizontal flipping



 Custom CNN Architecture
The CNN model comprises:
- Multiple convolutional layers with ReLU activation.
- Max-pooling layers for feature reduction.
- Dense layers with dropout for overfitting control.
- Softmax output for classification.



 Results

 Four-Class Classification
- Accuracy: 86%
- Challenge: Poor performance on Moderate Demented class due to limited data.

 Three-Class Classification
- Accuracy: 98%
- Observation: Simplifying class structure improved accuracy.

 Pretrained Model Performance
- Residual Net: Best accuracy at 64.21%.
- Efficient Net: Moderate performance, 51.50%.
- Mobile Net: Accuracy of 56.74%.



 Streamlit Interface
A Streamlit-based GUI allows users to:
- Upload MRI images.
- Perform classification with trained models.
- Visualize results interactively.



 Future Work
- Expand datasets with diverse imaging modalities (e.g., PET scans).
- Integrate advanced architectures like Vision Transformers.
- Employ explainability tools like Grad-CAM and SHAP.
- Explore federated learning for privacy-preserving training.



 Installation and Usage
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/alzheimers-classification.git
   ```
2. Navigate to the project directory:
   ```bash
   cd alzheimers-classification
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the Streamlit interface:
   ```bash
   streamlit run app.py
   ```



 Contributing
Contributions are welcome! Feel free to fork the repository and submit pull requests.



 License
This project is licensed under the MIT License. See the `LICENSE` file for more details.



 Acknowledgments
- Pretrained models from [ImageNet](https://www.image-net.org/).
- Libraries: TensorFlow, Keras, Streamlit.

