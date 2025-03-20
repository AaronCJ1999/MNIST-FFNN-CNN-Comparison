MNIST-FFNN-CNN-Comparison

A comparative analysis of Feedforward Neural Networks (FFNN) and Convolutional Neural Networks (CNN) for handwritten digit classification using the MNIST dataset.

Overview

This repository provides implementations of both FFNN and CNN architectures for the MNIST dataset. It demonstrates how to:
	•	Load and preprocess the MNIST dataset using idx2numpy.
	•	Build and train a FFNN with a simple dense architecture.
	•	Build and train a CNN optimized for efficient performance.
	•	Evaluate and compare the test accuracy and loss of each model.

Repository Structure
├── README.md
├── main.py                # Main script containing both FFNN and CNN implementations
├── train-images.idx3-ubyte  # MNIST training images (IDX format)
├── train-labels.idx1-ubyte  # MNIST training labels (IDX format)
├── t10k-images.idx3-ubyte   # MNIST test images (IDX format)
└── t10k-labels.idx1-ubyte   # MNIST test labels (IDX format)

Installation:

1. Clone the repository: 
git clone https://github.com/yourusername/MNIST-FFNN-CNN-Comparison.git
cd MNIST-FFNN-CNN-Comparison

2. Create a virtual environment (optional but recommended):
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

3. Install the required dependencies:
pip install numpy tensorflow idx2numpy


Usage:

To run the experiments, simply execute the main script:

The script will:
	•	Load and normalize the MNIST dataset.
	•	Train the FFNN model for 10 epochs and print the accuracy and loss.
	•	Train the CNN model for 10 epochs and print the accuracy and loss.
	•	Output a summary of the test accuracy and loss for both models.

Experiment Details
	•	FFNN Model:
	•	Architecture: Flatten → Dense(128, ReLU) → Dense(64, ReLU) → Dense(10, Softmax)
	•	Optimizer: Adam (learning rate: 0.0005)
	•	Loss Function: Sparse Categorical Crossentropy
	•	CNN Model:
	•	Architecture: Conv2D(32, 3x3, ReLU) → MaxPooling2D → Conv2D(64, 3x3, ReLU) → MaxPooling2D → Flatten → Dense(64, ReLU) → Dense(10, Softmax)
	•	Optimizer: Adam (learning rate: 0.0005)
	•	Loss Function: Sparse Categorical Crossentropy

Contributing

Feel free to fork the repository, open issues, or submit pull requests. Contributions that improve model performance, add new features, or enhance documentation are welcome!




