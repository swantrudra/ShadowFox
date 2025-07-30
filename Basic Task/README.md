
# CIFAR-10 Image Classification with CNN (TensorFlow/Keras)

This project demonstrates image classification on the CIFAR-10 dataset using a Convolutional Neural Network (CNN) implemented with TensorFlow and Keras. The CIFAR-10 dataset contains 60,000 32x32 color images in 10 different classes.

## 📌 Project Overview
The CNN model is trained to classify images into one of the following categories:
- airplane
- automobile
- bird
- cat
- deer
- dog
- frog
- horse
- ship
- truck

## 🔧 Technologies Used
- Python
- TensorFlow / Keras
- NumPy
- Matplotlib

## 🗂 Dataset
The CIFAR-10 dataset is loaded using TensorFlow's built-in datasets module:
```python
from tensorflow.keras import datasets
(X_train, y_train), (X_test, y_test) = datasets.cifar10.load_data()
```

## 🧠 Model Architecture
The CNN consists of:
- Conv2D (32 filters, 3x3 kernel, ReLU activation)
- MaxPooling2D
- Conv2D (64 filters, 3x3 kernel, ReLU activation)
- MaxPooling2D
- Flatten layer
- Dense (64 units, ReLU activation)
- Output Dense (10 units, softmax activation)

## ⚙️ Training
- Optimizer: Adam
- Loss Function: Sparse Categorical Crossentropy
- Metrics: Accuracy
- Epochs: 10

```python
cnn.compile(optimizer='adam',
            loss='sparse_categorical_crossentropy',
            metrics=['accuracy'])

cnn.fit(X_train, y_train, epochs=10)
```

## 📊 Evaluation
Model performance is evaluated using:
```python
cnn.evaluate(X_test, y_test)
```

## 🔍 Predictions
The model's predictions are converted from probability vectors to class labels using:
```python
y_classes = [np.argmax(element) for element in y_pred]
```

## 🖼 Sample Visualization
Images and their predicted/true labels can be visualized using:
```python
def plot_sample(X, y, index):
    plt.figure(figsize=(15,2))
    plt.imshow(X[index])
    plt.xlabel(classes[y[index]])
```

## 📁 How to Run
1. Make sure TensorFlow, NumPy, and Matplotlib are installed.
2. Run the Python script in a Jupyter notebook or Python environment.
3. The script will train a CNN model and output evaluation results and sample predictions.

## 📜 License
This project is open-source and available under the MIT License.
