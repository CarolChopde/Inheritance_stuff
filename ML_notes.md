# DEEP LEARNING COURSE (1,2,5) - Coursera
Course 1 - Neural Networks & Deep Learning
Course 2 - Improving Deep Neural Networks : Hyperparameters, tuning, regularization & Optimization
Course 5 - NLP : building sequence models

# Course 1

## What is a Neural Network?

A neural network consists of layers of nodes, or artificial neurons—an input layer, one or more hidden layers, and an output layer. Each node connects to others and has its own associated weight and threshold. If the output of a node exceeds a specified threshold, it activates, sending data to the next layer; otherwise, no data is passed along.
Every neural network consists of layers of nodes, or artificial neurons—an input layer, one or more hidden layers, and an output layer. 

### Linear Regression

**Linear regression** helps predict a dependent variable \(y\) based on an independent variable \(x\), after training on existing labeled data. It is a form of supervised machine learning suitable for continuous data (infinite values) but not ideal for categorical data (finite, distinct values).

#### Key Concepts:

- **Independent Variable**: \(x\)
- **Dependent Variable**: \(y\)
- **Model Parameters**: \(a_0\) (intercept) and \(a_1\) (slope), or \(\alpha\) and \(\beta\).

#### How It Works:

1. **Model Representation**:
   \[
   y = a_0 + a_1x
   \]
   For multiple features:
   \[
   y = a_0 + a_1x_1 + a_2x_2 + \ldots + a_nx_n
   \]

2. **Cost Function**: The mean squared error (MSE) measures the difference between actual and predicted values:
   \[
   \text{MSE} = \frac{1}{n} \sum (y_i - \hat{y}_i)^2
   \]
   The goal is to minimize MSE.

3. **Optimization**: Parameters are adjusted during training using techniques like gradient descent.

4. **Prediction**: The model can predict \(y\) for new input values.


### Key Concepts:

- **ReLU (Rectified Linear Unit)**: An activation function that outputs the input directly if it's positive; otherwise, it outputs zero.
  
- **Model**: A mathematical representation of a real-world process, expressed as an input-output relationship.

- **Linear Regression**: A supervised learning method used to predict a dependent variable \(y\) based on an independent variable \(x\). The model can be represented as:
  \[
  y = a_0 + a_1x
  \]
  For multiple features, it expands to:
  \[
  y = a_0 + a_1x_1 + a_2x_2 + \ldots + a_nx_n
  \]

- **Cost Function**: Used to identify the best-fitting function by minimizing the sum of squared residuals (distances from the line to data points).

- **Activation Function**: Determines the output of a node. If it exceeds a threshold, the node “fires,” passing data to the next layer, defining a feedforward network.

### Data Types:
- **Structured Data**: Organized databases.
- **Unstructured Data**: Raw formats like audio, images, and text.

### RNNs and CNNs:
- **Recurrent Neural Networks (RNNs)**: processes sequences of data, making them suitable for tasks like language modeling and time series prediction. (temporal data)
  
- **Convolutional Neural Networks (CNNs)**: Primarily used for image processing tasks, leveraging spatial hierarchies in data.They use layers that apply filters to detect patterns, like edges or shapes. This makes CNNs great for image classification, object detection, and similar tasks.

