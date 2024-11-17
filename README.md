# Classification-with-neural-network

## Overview
The goal of this project is to classify food products manufactured by three different producers using chemical characteristics. It involves data preprocessing, model construction, training, evaluation, and optimization.

## Dataset
The dataset contains the chemical characteristics of food products produced by three manufacturers. It includes 178 entries with 13 features such as amino acid, malic acid, ash, magnesium (Mg), phenols, and more. The target variable is the "Producer" column which identifies the manufacturer.

## Project Steps
### 1. Data Preparation
- **Importing Dataset**: The dataset is imported from a CSV file, and the first row is used as the column name.
- **Data Preprocessing**:
  - Missing Data Handling: Rows with NaN values were dropped.
  - Normalization: The features were normalized to ensure consistency in data scale.
  - Splitting: The dataset was split into training and testing sets with a ratio of 75:25.
  - Cross-Validation: 5-fold cross-validation was used.

### 2. Model Construction
- **Loss Function**: Softmax cross-entropy loss was used for this multi-class classification.
- **Network Design**: A fully connected artificial neural network with two hidden layers and one output layer was designed. ReLU activation was used in the hidden layers, while softmax was used for the output layer.

### 3. Model Training
- **Training Process**: Mini-batch stochastic gradient descent and Adam optimizer were used.
- **Parameters**: Different learning rates (`0.001`, `0.01`, `0.1`) and numbers of neurons (`32`, `64`, `128`) were tested.

### 4. Evaluation
- **Metrics**: The model was evaluated using accuracy, confusion matrix, and ROC curves. The metrics like precision, sensitivity, specificity, and accuracy were calculated for each class.

## Results
- The best model achieved an accuracy of `0.993` for learning rate `0.01` and `32` neurons.
- Regularization methods (Ridge and Lasso Regression) were also tested, but did not improve the model significantly.

## Requirements
- Python 3.x
- Libraries: `numpy`, `pandas`, `scikit-learn`, `matplotlib`

## Usage
1. Clone the repository:
   ```
   git clone <repository-url>
   ```
2. Install the required packages:
   ```
   pip install -r requirements.txt
   ```
3. Run the model training script:
   ```
   python train_model.py
   ```

## Conclusion
The model demonstrates good accuracy in classifying the products of all three producers, with particularly strong results for Producer 3. Improvements could be made to enhance sensitivity for Producer 1 and precision for Producer 2.
