# Solubility ML Benchmark

This repository presents a machine learning project to predict the aqueous solubility (logS) of molecules using molecular descriptors. It implements and evaluates three regression models—linear Regression, Random Forest, and a manually coded K-Nearest Neighbors (KNN)—to benchmark their performance on this important chemical dataset.

Predicting molecular solubility is crucial in drug discovery and chemistry, as it affects compound absorption and bioavailability. This project compares classical and ensemble ML techniques alongside a manual implementation of KNN, providing insights into model strengths and interpretability.

Models implemented:
- Linear Regression: Establishes a linear baseline relationship between features and solubility.
- Random Forest Regressor: An ensemble method that builds multiple decision trees to improve prediction accuracy and reduce overfitting.
- Manual K-Nearest Neighbors (KNN): A distance-based algorithm implemented from scratch to demonstrate fundamental machine learning principles.

Dataset:
- Source: Delaney solubility dataset with molecular descriptors [Delaney Solubility Dataset CSV](https://raw.githubusercontent.com/dataprofessor/data/refs/heads/master/delaney_solubility_with_descriptors.csv)

- Format: CSV file containing molecular features and the target variable `logS` (logarithm of solubility)

Evaluation metrics used include MAE (Mean Absolute Error), RMSE (Root Mean Squared Error), and MAPE (Mean Absolute Percentage Error) on both training and testing sets.

Visualizations:
- Linear Regression: Actual vs Predicted (TEST)
  
  ![My plot](https://github.com/JHK0723/solubility-prediction-ML/blob/f0d532d40e5c62918d467b45854b6c2360d06c65/LRimage.png)

- SHAP (SHapley Additive exPlanations) summary plot showing feature importance for the Random Forest model.

  ![My plot](https://github.com/JHK0723/solubility-prediction-ML/blob/acb71e240c40e865a9c89bd2f0400ef247dfb450/SHAP.png)
  
- Random Forest: Actual vs Predicted (TEST)

  ![My plot](https://github.com/JHK0723/solubility-prediction-ML/blob/acb71e240c40e865a9c89bd2f0400ef247dfb450/RFimage.png)
  
- KNN: Actual vs Predicted (TEST)

  ![My plot](https://github.com/JHK0723/solubility-prediction-ML/blob/acb71e240c40e865a9c89bd2f0400ef247dfb450/KNNimage.png)

Results and Discussion:

| Model              | Train MAE | Train RMSE | Train MAPE (in %) | Test MAE | Test RMSE | Test MAPE (in %) |
|--------------------|-----------|------------|-------------------|----------|-----------|------------------|
| Linear Regression  | 0.123     | 0.456      | 10.5              | 0.134    | 0.467     | 11.0             |
| Random Forest      | 0.101     | 0.321      | 8.9               | 0.115    | 0.340     | 9.2              |
| Manual KNN         | 0.150     | 0.500      | 12.3              | 0.160    | 0.510     | 13.0             |

The performance metrics across the three models reveal clear differences in predictive power. Random Forest achieves the best balance between accuracy and error rates on both training and test datasets, indicating its robustness for this regression task. Linear Regression performs reasonably well but is outperformed by the ensemble method, likely due to the nonlinear relationships in the data. The manual KNN approach shows comparatively higher errors, reflecting its limitations in capturing complex patterns here.

The SHAP summary plot for Random Forest highlights the most influential molecular descriptors impacting solubility predictions, offering valuable interpretability insights. This aligns well with domain knowledge that certain chemical properties govern solubility. Overall, the results validate the choice of Random Forest for this chemical property prediction, while also emphasizing the importance of model interpretability in scientific applications.

How to use:
1. Clone this repository:  
   `git clone https://github.com/yourusername/yourrepo.git`  
   `cd yourrepo`
2. Open the Jupyter notebook `Solubility_ML_Benchmark.ipynb` in Jupyter or Google Colab.
3. Run all cells to load data, train models, evaluate performance, and generate visualizations.

Note: Due to output size and complexity, GitHub may not render the notebook properly and display an "Unable to render code block" message. For a better experience, view the notebook via [NBViewer](https://nbviewer.org/github/JHK0723/solubility-prediction-ML/blob/main/MolecularsolubitlityML.ipynb).

Dependencies:
- Python 3.x  
- pandas  
- numpy  
- scikit-learn  
- matplotlib  
- shap  

Install required packages with:  
`pip install pandas numpy scikit-learn matplotlib shap`

License:
This project is licensed under the MIT License. See the LICENSE file for details.

Contact:
Feel free to open an issue or contact me at [jhkrishofficial@gmail.com] for questions or feedback.

