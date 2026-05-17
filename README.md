# Part 1: Neural Network Fundamentals and Training Behavior Analysis

## Project Overview

This project focuses on developing and evaluating a feed-forward neural network using a customer churn dataset. The primary objective of the project was to understand how neural networks learn through forward propagation, backpropagation, loss computation, and parameter optimization.

The implementation was carried out using Python along with TensorFlow/Keras, Pandas, Scikit-learn, Matplotlib, and Seaborn.

---

## Dataset Information

Dataset Used: Customer Churn Dataset

The dataset contains customer-related attributes such as subscription details, payment methods, contract information, and customer behavior patterns. The target variable used for prediction is:

- `churn`
    - 0 → Customer retained
    - 1 → Customer churned

Dataset Source Link:

https://drive.google.com/drive/folders/1akV6po4Nrgkc3yQrJkzA6cJlV-wBvUYs?usp=sharing

---

## Task 1: Dataset Understanding

The dataset was analyzed using Pandas functions to examine:

- Total number of rows and columns
- Feature data types
- Missing values
- Statistical summary
- Distribution of the target variable

A churn distribution visualization was created to study class imbalance within the dataset.

### Observation

The dataset was highly imbalanced because the majority of customers belonged to the non-churn category, while only a small number of customers were classified as churn customers.

---

## Task 2: Data Preprocessing

The following preprocessing operations were performed:

- Checked and handled missing values
- Encoded categorical columns using Label Encoding
- Removed unnecessary features such as `customer_id`
- Standardized numerical features using `StandardScaler`
- Split the dataset into training and testing sets using an 80:20 ratio

---

## Task 3: Neural Network Model Building

A feed-forward neural network was developed using the TensorFlow/Keras Sequential API.

### Model Architecture

- Input Layer
- Hidden Layer 1 → 16 neurons with ReLU activation
- Hidden Layer 2 → 8 neurons with ReLU activation
- Output Layer → 1 neuron with Sigmoid activation

### Optimizer and Loss Function

- Optimizer: Adam
- Loss Function: Binary Crossentropy

---

## Task 4: Training and Evaluation

The model was trained using the training dataset and evaluated on the testing dataset.

### Evaluation Techniques Used

- Training Accuracy
- Validation Accuracy
- Testing Accuracy
- Confusion Matrix
- Classification Report

### Observation

The model achieved high testing accuracy; however, due to the class imbalance, it struggled to correctly identify churn customers. Metrics such as precision, recall, and F1-score were therefore important for evaluating the model more effectively.

---

## Task 5: Hyperparameter Experimentation

Three different experiments were conducted by modifying:

- Number of hidden layers
- Number of neurons
- Activation functions
- Learning rate
- Batch size
- Number of epochs

### Best Performing Model

Experiment 2 delivered the best performance with:

- 2 hidden layers
- 32 and 16 neurons
- ReLU activation
- 30 epochs

---

## Task 6: Final Reflection

This project helped develop understanding of several important neural network concepts, including:

- The role of weights and biases
- The importance of activation functions
- The impact of learning rate on model training
- Underfitting and overfitting behavior
- The effect of imbalanced datasets on prediction performance

The project also demonstrated that accuracy alone is not always sufficient for evaluating classification models.

---

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- TensorFlow / Keras

---

## Repository Structure

```bash
part-1-neural-network-analysis/
│
├── README.md
├── notebook.ipynb
├── requirements.txt
└── results/
    ├── model_comparison_table.csv
    └── evaluation_outputs.png
```

---

## Conclusion

This project provided practical understanding of neural network fundamentals and model training behavior. The hyperparameter experiments helped demonstrate how different model architectures and training configurations can influence prediction performance.
