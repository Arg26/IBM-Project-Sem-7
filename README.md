
# Fashion-MNIST Image Classifier 👕👟

## 📌 Overview

The Fashion-MNIST Image Classifier is a deep learning project that uses a Convolutional Neural Network (CNN) built with TensorFlow and Keras to classify clothing images into 10 different categories.

The project covers the complete machine learning workflow, including data preprocessing, model building, training, evaluation, visualization, and prediction on custom images.

## ✨ Features

- Data loading and preprocessing using Pandas and NumPy.
- Visualization of sample images and class distribution.
- CNN-based image classification using TensorFlow and Keras.
- Data augmentation to improve generalization.
- Batch normalization and dropout to help reduce overfitting.
- Early stopping and model checkpointing.
- Training and validation accuracy and loss graphs.
- Model evaluation using test accuracy, classification reports, and confusion matrices.
- Visualization of incorrectly classified images.
- Saving the trained model for future use.
- Prediction on custom clothing images.

## 📊 Dataset

This project uses the Fashion-MNIST dataset containing 70,000 grayscale images.

| Property | Description |
|---|---|
| Training images | 60,000 |
| Test images | 10,000 |
| Image dimensions | 28 × 28 pixels |
| Image channels | 1 (grayscale) |
| Number of classes | 10 |
| Data format | CSV |

Each CSV file contains one label column and 784 pixel-value columns representing a 28 × 28 image.

### Clothing Categories

| Label | Category |
|---|---|
| 0 | T-shirt/top |
| 1 | Trouser |
| 2 | Pullover |
| 3 | Dress |
| 4 | Coat |
| 5 | Sandal |
| 6 | Shirt |
| 7 | Sneaker |
| 8 | Bag |
| 9 | Ankle boot |

## 🛠️ Technologies Used

- **Python**
- **TensorFlow**
- **Keras**
- **NumPy**
- **Pandas**
- **Matplotlib**
- **Scikit-learn**
- **Pillow (PIL)**
- **Jupyter Notebook**
- **Google Colab**

## 🧠 Model Architecture

The project uses a Convolutional Neural Network designed to extract visual features and classify clothing images.

The architecture includes:

- Convolutional layers with 32, 64, and 128 filters.
- Batch normalization layers.
- ReLU activation functions.
- Max-pooling layers.
- Dropout for regularization.
- Global average pooling.
- A dense layer with 128 neurons.
- A softmax output layer with 10 classes.

### Model Configuration

- **Optimizer:** Adam
- **Learning rate:** 0.001 initially
- **Loss function:** Sparse categorical cross-entropy
- **Metric:** Accuracy
- **Maximum epochs:** 40
- **Batch size:** 128
- **Validation split:** 10% of the supplied training data

The model uses data augmentation, early stopping, learning-rate reduction, and checkpointing to help improve generalization and retain the best-performing checkpoint.

## 🔄 Project Workflow

1. Load the training and test CSV files.
2. Inspect the dataset structure and class distribution.
3. Normalize pixel values to the range 0–1.
4. Reshape images into 28 × 28 grayscale tensors.
5. Split the training data into training and validation subsets.
6. Build and compile the CNN.
7. Train the model using validation monitoring and callbacks.
8. Plot training and validation accuracy and loss.
9. Evaluate the model on the held-out test dataset.
10. Generate a classification report and confusion matrix.
11. Visualize incorrectly classified examples.
12. Save the trained model.
13. Upload a custom image and generate a prediction.

## 🚀 Getting Started

### Prerequisites

Install Python and the required libraries, or use Google Colab.

### 1. Clone the Repository

```bash
git clone <your-repository-url>
cd <your-repository-folder>
```

Replace the placeholders with your actual GitHub repository URL and folder name.

### 2. Install Dependencies

```bash
pip install tensorflow numpy pandas matplotlib scikit-learn pillow
```

### 3. Prepare the Dataset

Place the following files inside the `dataset` directory:

```text
dataset/
├── fashion-mnist_train.csv
└── fashion-mnist_test.csv
```

The CSV files should contain the label column followed by the 784 pixel columns.

### 4. Open the Notebook

Open `Fashion_MNIST_Training.ipynb` using Jupyter Notebook, JupyterLab, or Google Colab.

Run the notebook cells sequentially, starting from the imports and dataset loading sections.

### 5. Configure Google Colab

If your dataset is stored in Google Drive, mount your Drive:

```python
from google.colab import drive
drive.mount('/content/drive')
```

Update the dataset paths in the notebook to match your folder structure.

For GPU acceleration, select:

**Runtime → Change runtime type → T4 GPU**

A GPU option may not always be available, depending on resource availability and account limits.

## 📈 Model Evaluation

The notebook evaluates the trained model using:

- **Test accuracy:** Overall proportion of correctly classified test images.
- **Test loss:** Measures prediction error on the test set.
- **Classification report:** Precision, recall, F1-score, and support for each category.
- **Confusion matrix:** Shows correct and incorrect predictions across all classes.
- **Learning curves:** Visualize training and validation accuracy and loss.
- **Error analysis:** Displays examples where the predicted category differs from the true label.

Record the actual test accuracy produced by your training run here:

**Test Accuracy:** Add your measured result after training.

## 🖼️ Custom Image Prediction

The notebook includes an image-upload feature that allows users to test their own clothing images.

The image is:

1. Uploaded through Google Colab.
2. Converted to grayscale.
3. Resized to 28 × 28 pixels.
4. Normalized to the range 0–1.
5. Passed to the trained CNN for classification.

The model returns the predicted clothing category and its confidence score.

**Important:** Fashion-MNIST contains small, centered grayscale images. Predictions on ordinary photographs may be less reliable because backgrounds, lighting, image orientation, and object placement can differ from the training data.

## 💾 Saved Models

The notebook saves the following model files:

| File | Description |
|---|---|
| `best_fashion_mnist.keras` | Best checkpoint selected using validation accuracy |
| `fashion_mnist_classifier.keras` | Saved trained model |

These files can be loaded later to make predictions without retraining the entire model.

## 📁 Project Structure

```text
fashion-mnist-project/
│
├── Fashion_MNIST_Training.ipynb
├── README.md
│
└── dataset/
    ├── fashion-mnist_train.csv
    └── fashion-mnist_test.csv
```

The trained model files are generated after training.

## 🔮 Future Improvements

- Experiment with deeper CNN architectures.
- Tune hyperparameters and learning-rate schedules.
- Improve preprocessing for real-world photographs.
- Explore transfer learning for more complex image classification tasks.
- Develop a web interface for interactive predictions.
- Deploy the trained model as a computer vision application.

## ⚠️ Limitations

- Perfect accuracy cannot be guaranteed.
- Some categories, such as Shirt, Coat, and Pullover, can be visually similar.
- Real-world images may differ significantly from the training dataset.
- A high confidence score does not guarantee a correct prediction.
- Actual model performance should be reported using measured evaluation results.

## 🎯 Conclusion

This project demonstrates an end-to-end deep learning pipeline for fashion image classification, from dataset preprocessing and CNN training to performance evaluation and custom image prediction.

It provides practical experience with convolutional neural networks, image preprocessing, model optimization, and computer vision.

---

**Developed using Python, TensorFlow, and Keras.**
