![Predicting Energy Intake from Recipe Ingredients](assets/images/github-header.png "Predicting Energy Intake from Recipe Ingredients")

# Model Card for Predicting Energy Intake from Recipe Ingredients

## Model Description

**Input:** The model inputs are vectorized representations of food names and food categories, using sklearn's `CountVectorizer`. This process transforms categorical text data into a numeric format that the model can effectively utilize for predictions.

**Output:** The output of this model is the predicted energy content measured in kilojoules (kJ). This estimation is vital for determining the caloric content of meals, aiding in nutritional planning and dietary assessments.

**Model Architecture:** This model is based on an XGBRegressor, a gradient boosting machine learning framework optimized for performance and speed. The specific hyperparameters tuned using Optuna are:
- `n_estimators`: 93
- `max_depth`: 42
- `grow_policy`: 'depthwise'

These settings were selected to balance the model's ability to learn detailed data patterns without excessively increasing computational demands.

## Performance

The XGBRegressor has demonstrated exceptional performance metrics on the training dataset:
- **Train Accuracy**: 99.883%
- **Train RMSE**: 40.4259
- **MSE**: 100474
- **RMSE**: 316.977
- **R2**: 0.780291
- **Variance**: 0.780765

These metrics indicate a high degree of accuracy and reliability, with the model explaining 
approximately 78.07% of the variance in the dependent variable, suggesting strong predictive 
capabilities.

## Limitations

The primary limitation of this model is its potential for overfitting due to the very high `max_depth` used during training. While this allows the model to learn complex patterns in the training data, it may not perform as well on unseen data if those patterns do not generalize. Additionally, the model's focus on food names and categories might overlook other influential nutritional factors, possibly affecting prediction accuracy in practical scenarios.

Please see the [datasheet](data_sheet.md "data sheet") for more detailed information on the 
dataset where various biases are discussed.

## Trade-offs

Choosing an XGBRegressor with extensive depth and a significant number of estimators provides high accuracy but might require considerable computational resources. This setup also complicates the model, potentially making it less interpretable to users or stakeholders who prefer a straightforward understanding of how predictions are made. The depth of the model may also lead to challenges in maintaining and updating the model as new types of data become available.