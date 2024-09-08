# Predicting Hazardous Near-Earth Objects (NEOs)
## Project Overview
This project aims to predict whether a Near-Earth Object (NEO) is classified as hazardous based on various features such as size, velocity, and orbital characteristics. By applying machine learning techniques, the model can offer valuable predictions that assist researchers and decision-makers in space exploration and planetary defense.

Table of Contents
1. Project Overview
2. Dataset
3. Modeling Approach
4. Evaluation
5. Results and Findings
6. Installation and Usage
7. Conclusion and Insights

## Dataset   
The dataset contains information about Near-Earth Objects (NEOs), including orbital parameters, size, velocity, and other relevant features. Here are the key features used in the model:
* Absolute Magnitude: Brightness of the NEO, where a lower magnitude implies a brighter and potentially larger object.
* Estimated Diameter (min/max): A range of the NEO's estimated size.
* Relative Velocity: The speed of the NEO relative to Earth.
* Miss Distance: The closest distance of the object to Earth.
* Orbiting Body: Indicates the celestial body the NEO is orbiting (generally the Sun).
* Target Variable: A binary label indicating whether the NEO is classified as hazardous (True) or not hazardous (False).
  
## Modeling Approach
To predict whether an NEO is hazardous, the following approach was taken:
1. Data Preprocessing:
* Missing Values: Addressed any missing data in key features.
* Scaling: Standardized continuous variables (e.g., diameter, velocity).
* Encoding: Categorical features were one-hot encoded as needed.

2. Feature Selection:
* Correlation Analysis: Used to identify relationships between features and the target variable.
* Feature Importance: Analyzed to identify the most influential features for prediction.
 
3. Model Selection:
* Random Forest Classifier: Chosen for its strong performance with classification tasks, particularly in handling imbalanced datasets and providing feature importance insights.
  
4. Model Training:
* Cross-validation was employed to avoid overfitting and to ensure that the model generalizes well.
  
5. Evaluation Metrics:
* Accuracy: Measures the overall correctness of the predictions.
* Precision, Recall, F1-score: Evaluate the model's ability to correctly classify hazardous NEOs.
* ROC-AUC: Assesses the model's ability to distinguish between the hazardous and non-hazardous classes.

## Evaluation
The model was evaluated based on several metrics, including accuracy, precision, recall, F1-score, and ROC-AUC. Below is a summary of the results:
* Random Forest Classifier achieved the highest performance with:
 * Accuracy: 100%
 * AUC Score: 100%
* Gradient Boosting: Slightly better precision, but lower recall compared to the Random Forest model.
  
## Results and Findings
Key insights from the project:
* Feature Importance: Orbital parameters such as semi-major axis and perihelion distance were the most influential features in predicting hazardous NEOs.
* Imbalanced Data: The dataset was highly imbalanced, with a small percentage of NEOs labeled as hazardous. Using resampling techniques like oversampling or undersampling improved model performance.
* Model Interpretability: The Random Forest model offered high accuracy and interpretability, allowing for a deeper understanding of which features most impacted the classification.
  
## Installation and Usage

To run this project on your local machine, follow the steps below:

### 1. Clone the Repository
First, clone the repository to your local machine using the following command:

```bash
git clone https://github.com/yourusername/neo-prediction.git

### 2. Install the necessary dependencies:

```bash
Copy code
pip install -r requirements.txt
Run the Jupyter notebook:

bash
Copy code
jupyter notebook predicting-hazardous-neos.ipynb
Follow the notebook's instructions to explore the data, train the models, and evaluate their performance.

## Conclusion and Insights
This project demonstrates that machine learning can effectively predict whether an NEO is hazardous based on a combination of physical and orbital parameters. The Random Forest model provided a high degree of accuracy and offered interpretable results, which could be beneficial for early warning systems in planetary defense.
