# Is this AI?
Current AI plagiarism checkers suck, so I built my own.

## Overview
This repository contains an AI-powered text detection model designed to classify text as either AI-generated or human-written. The project is organized into two main directories:
- `Model`: Contains the code and resources for training and deploying the AI text detector.
- `Data`: Includes the dataset used for training and evaluating the model.

## Repository Structure
```
├── Model/
│   ├── ai_text_detector.ipynb    # Jupyter Notebook for model development and experimentation
│   ├── ai_text_detector_model.h5 # Trained model file
│   └── README.md                 # Documentation for the Model directory
│
├── Data/
│   └── README.md                 # Documentation for the Data directory, and link to the dataset.
│
└── README.md                     # Main project documentation
```

## Getting Started

### Prerequisites
- Python 3.x
- [pip](https://pip.pypa.io/en/stable/installation/)

### Installation
1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/ai-text-detector.git
   cd ai-text-detector/Model
   ```
2. **Set up a virtual environment (optional but recommended)**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```
3. **Install the required dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

### Model Training and Evaluation
1. **Navigate to the `Model` directory**:
   ```bash
   cd Model
   ```
2. **Open the Jupyter Notebook**:
   ```bash
   jupyter notebook ai_text_detector.ipynb
   ```
   Follow the steps in the notebook to preprocess the data, train the model, and evaluate its performance.


## Dataset
The dataset used in this project is the ["AI vs Human Text" dataset](https://www.kaggle.com/datasets/shanegerami/ai-vs-human-text/data), which comprises approximately 500,000 essays, both AI-generated and human-written. Detailed information about the dataset and its structure can be found in the `Data/README.md` file.

## Model Details
- **Architecture**: The model is based on a **Bidirectional LSTM** architecture, including:
  - An embedding layer for token and position embeddings.
  - A Bidirectional LSTM with 32 units, `tanh` activation, and L2 regularization.
  - A Dense layer with a sigmoid activation function for binary classification.
  - Optimized using the Adam optimizer with a learning rate of `3e-4`.
- **Performance**: The model achieves an accuracy of **99.8%** on the test set.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or suggestions.

## License
This project is licensed under the MIT License.

## Acknowledgments
- Dataset curated by [Shane Gerami](https://www.kaggle.com/shanegerami).
- Inspired by recent advancements in AI text detection.
- Built using TensorFlow, Pandas, Kaggle GPUs, boredom and coffee.
