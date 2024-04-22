# Model Card for Predicting Energy Intake from Recipe Ingredients

## Model Description

**Input:** The model inputs consist of food names and food categories. These inputs are vectorized using sklearn's `CountVectorizer`, which converts the text data into a numeric form that the model can process. This transformation allows the model to analyze the frequency of words and use this information to predict Energy (kJ) content.

**Output:** The model outputs an estimation of the Energy content in kilojoules (kJ). This predicted value serves as an indicator of the nutritional value, specifically the calorie content, which is crucial for dietary management and meal planning.

**Model Architecture:** The model uses an XGBRegressor, a type of gradient boosting framework that is efficient for structured data. The model was hyperparameter tuned using Optuna with the following settings: `n_estimators` set to 196, `max_depth` of 88, and a `grow_policy` of 'depthwise'. This configuration was chosen to optimize prediction accuracy and manage computational efficiency.

## Performance

The performance of the XGBRegressor was primarily evaluated using Root Mean Square Error (RMSE) and R-squared (R2) metrics on the training data. During hyperparameter optimization (HPO), the objective was to minimize the RMSE, which resulted in a model with an RMSE of 323.864 and an impressive R2 of 0.7707, indicating that approximately 77.07% of the variance in the Energy (kJ) content is predictable from the input features.

## Limitations

While the XGBRegressor performs well on training data, its performance on unseen data needs to be thoroughly tested to ensure generalizability. The model may also be sensitive to overfitting due to the large `max_depth` used during training. Additionally, since the input features are limited to food names and categories, the model might not capture other influential factors such as cooking methods or ingredient interactions, which can affect the Energy (kJ) content of dishes.

## Trade-offs

The choice of a deep and complex model like the XGBRegressor with an extensive depth and large number of estimators ensures a high level of accuracy but comes at the cost of increased computational resources and potential overfitting. While the model can capture complex nonlinear relationships in the data, it may require careful monitoring and regular updates to adapt to new data or changes in dietary trends. Moreover, the model’s complexity can make it less interpretable, which might be a drawback in applications where understanding the decision-making process is crucial. 
