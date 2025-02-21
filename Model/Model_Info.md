# Is this AI?

## Overview
This repository contains an AI-powered text detection model designed to classify text as either AI-generated or human-written. The model utilizes deep learning techniques to analyze linguistic patterns and distinguish between different text sources.

## Features
- **Binary Classification**: Determines whether a given text is AI-generated or written by a human.
- **Deep Learning-Based**: Leverages state-of-the-art natural language processing (NLP) techniques.
- **Customizable**: Can be fine-tuned with additional datasets to improve performance.
- **Jupyter Notebook Implementation**: Easy to modify and run experiments.

## Installation
To set up the project, follow these steps:

```bash
# Clone the repository
git clone https://github.com/yourusername/ai-text-detector.git
cd ai-text-detector

# Create a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

# Install dependencies
pip install -r requirements.txt
```

## Usage
Run the Jupyter Notebook to test the model:

```bash
jupyter notebook ai-text-detector.ipynb
```

Modify the notebook to input your own text samples and evaluate results.

## Model Details
- **Architecture**: The model is based on a **Bidirectional LSTM** architecture. It includes:
  - An **embedding layer** for token and position embeddings.
  - A **Bidirectional LSTM** with 32 units, `tanh` activation, and L2 regularization.
  - A **Dense layer** with a sigmoid activation function for binary classification.
  - Optimized using **Adam optimizer** with a learning rate of `3e-4`.
- **Training Data**: Trained on a dataset of AI-generated and human-written text.
- **Evaluation Metrics**: Accuracy, precision, recall, and F1-score.
- **Accuracies**: The model achieves an accuracy of **99.8%** on the test set.

## Contributing
Contributions are welcome! Feel free to open issues and submit pull requests.

## License
This project is licensed under the MIT License.

## Acknowledgments
- Inspired by recent advancements in AI text detection.
- Built using TensorFlow, Pandas, and Kaggle GPUs.

