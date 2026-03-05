# AI Approach for Reliability Estimation of Safety-Critical Systems

## Overview

This project explores the use of **Artificial Intelligence and Deep Learning techniques** to improve the **reliability of safety-critical software systems** through **Software Fault Prediction (SFP)**.  

Software faults significantly reduce system reliability and increase development and maintenance costs. By applying machine learning and deep learning models, this project predicts faulty software modules early in the development lifecycle, enabling developers to prioritize testing and improve software quality.

The study evaluates multiple deep learning models including **Multi-Layer Perceptron (MLP), Convolutional Neural Networks (CNN), and Recurrent Neural Networks (RNN)** using datasets from NASA’s Metrics Data Program. 

---

## Project Objectives

- Predict software defects in safety-critical systems
- Improve software reliability through early fault detection
- Evaluate the effectiveness of deep learning models for Software Fault Prediction
- Compare different models and hyperparameter configurations
- Analyze performance across multiple NASA software datasets

---

## Dataset

The project uses publicly available datasets from the **NASA Metrics Data Program (MDP)** repository. 

These datasets contain software module metrics and defect labels.

### Datasets Used

| Dataset | Instances | Language | Description |
|-------|--------|---------|-------------|
| CM1 | 344 | C | NASA spacecraft instrument |
| PC1 | 759 | C | Satellite flight software |
| MW1 | 264 | C | Zero-gravity combustion experiment |
| MC1 | 9466 | C/C++ | Ground data storage management |

Each dataset contains **20 static code metrics**, including:

- Lines of Code (LOC)
- Cyclomatic Complexity
- Halstead Metrics
- Design Complexity
- Branch Count
- Unique Operators / Operands

These metrics capture structural properties of software modules used to predict defects. 

---

## Methodology

The Software Fault Prediction framework consists of two major phases:

### 1. Training Phase

- Data preprocessing
- Dataset balancing using **SMOTE**
- Feature extraction from static code metrics
- Model training using deep learning algorithms

### 2. Validation Phase

Models are evaluated using classification performance metrics derived from the **confusion matrix**.

Evaluation metrics include:

- Accuracy
- Precision
- Recall / Detection Rate
- True Negative Rate
- F1 Score

---

## Models Implemented

### Multi-Layer Perceptron (MLP)

A feedforward neural network trained using backpropagation to learn complex relationships between software metrics and defect probability.

### Convolutional Neural Network (CNN)

A deep learning model capable of detecting patterns within structured data representations of software metrics.

### Recurrent Neural Network (RNN)

RNN models capture **temporal and sequential relationships** in data, enabling prediction of faults based on historical patterns. 

---

## Hyperparameter Optimization

The models were tuned using various hyperparameters including:

- Number of training epochs
- Activation functions  
  - ReLU  
  - Tanh  
  - Sigmoid  
  - Swish
- Optimizers  
  - Adam  
  - SGD  
  - Adagrad

Hyperparameter tuning was performed through extensive experimentation to identify the optimal configuration for each dataset.

---

## Results

Model performance was evaluated across four datasets using multiple evaluation metrics.

### Best Accuracy Results

| Dataset | Best Model | Mean Accuracy |
|------|------|------|
| CM1 | CNN | 0.974 |
| MC1 | MLP | 0.977 |
| PC1 | CNN | 0.974 |
| MW1 | CNN | 0.974 |

### Best Precision Results

| Dataset | Model | Precision |
|------|------|------|
| CM1 | MLP | 0.888 |
| MC1 | MLP | 0.773 |
| PC1 | MLP | 0.917 |
| MW1 | MLP | 0.929 |

Overall, **MLP demonstrated strong precision and F1-scores**, while **CNN achieved consistently high accuracy across datasets**. 

---

## Technologies Used

- Python
- Keras
- Scikit-learn
- NumPy
- Pandas
- Matplotlib

---

## System Requirements

- Python 3.6+
- Minimum 8GB RAM
- CPU/GPU capable of training deep learning models

---

## Key Contributions

- Applied deep learning models to software defect prediction
- Performed hyperparameter experimentation across multiple architectures
- Compared MLP, CNN, and RNN models for reliability estimation
- Demonstrated improved prediction performance using optimized configurations

---

## Limitations
- The models rely on static code metrics, which do not capture semantic understanding of source code.
- Dataset imbalance required additional preprocessing using SMOTE.

---

## Future Work

- Future improvements could include:
- Using transformer-based models or large language models to analyze code semantics
- Incorporating code embeddings
- Using larger industrial datasets
- Building automated defect prediction pipelines

---

## Contributors

- Romith Bondada
- Sukanya Karasala
- Aman Abdul Rasheed
- Sai Sushrooth Chand


SRM University-AP
Department of Computer Science & Engineering

---


## License
This project is for academic and research purposes.

---

## References
NASA Metrics Data Program (MDP) Repository
