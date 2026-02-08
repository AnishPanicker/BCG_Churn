PowerCo Customer Churn Prediction
BCG Gamma Virtual Experience Project

📌 Project Overview
The objective of this project is to investigate price sensitivity as a potential driver for customer churn at PowerCo, a major energy utility provider. Using a dataset of approximately 14,000 customers, I built a predictive model to identify customers at high risk of leaving.

🛠️ Tech Stack
Language: Python

Environment: Google Colab / Jupyter

Libraries: TensorFlow/Keras, Pandas, Scikit-Learn, Seaborn

📊 Data Engineering & Preprocessing
To prepare the raw utility data for a Neural Network, I performed the following:

Feature Transformation: Converted raw dates into seasonal features (Month of renewal/modification) to capture time-based churn patterns.

Categorical Encoding: Applied OneHotEncoding to campaign origins and sales channels.

Handling Imbalance: Utilized Stratified Splitting to maintain the 10% churn ratio across training and testing sets.

Feature Scaling: Used StandardScaler to normalize high-variance features (like energy consumption) for stable Neural Network convergence.

🧠 Modeling Approach
I implemented a Sequential Neural Network using TensorFlow:

Input Layer: Dynamic shape based on preprocessed features.

Hidden Layer: 20 neurons with ReLU activation.

Output Layer: 1 neuron with Sigmoid activation to output churn probability (0 to 1).

Loss Function: Binary Crossentropy (ideal for binary classification).

📈 Key Results
Primary Metric: AUC-ROC / Recall (to prioritize catching actual churners).

Key Insight: While price sensitivity is a factor, seasonal contract renewal months and contract duration were significant predictors.
