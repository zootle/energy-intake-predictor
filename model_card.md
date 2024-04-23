# Model Card for Predicting Energy Intake from Recipe Ingredients

## Model Type

RandomForestRegressor (scikit-learn v1.4.2)

## Model Description

The RandomForestRegressor is a meta estimator that fits a number of decision tree regressors on 
various sub-samples of 
the dataset and uses averaging to improve the predictive accuracy and control over-fitting.

**Input:** The inputs to this model include food names and food categories, which are 
transformed into numerical representations using the `CountVectorizer` from sklearn. This 
process allows the model to process categorical textual data and identify patterns related to 
the energy content in ingredient names.

**Output:** The model predicts the energy content in kilojoules (kJ) based on the input features.
This predicted value, `Energy (kJ)` is critical for assessing the caloric content of recipes, 
aiding in 
dietary planning and nutritional analysis.

**Model Architecture:** The model employs a RandomForestRegressor, an ensemble learning method 
based on decision trees. It was hyperparameter tuned using Optuna with the following configuration:
- `n_estimators`: 66
- `min_samples_split`: 2
- `max_depth`: 244
- `min_samples_leaf`: 1

These parameters were optimized to enhance the model's ability to capture complex patterns in the data while maintaining robustness against overfitting.

## Performance

The RandomForestRegressor has achieved strong performance:
- **Train Accuracy**: 96.4715%
- **Train RMSE**: 117.943
- **MSE**: 92,345.8
- **RMSE**: 303.884
- **R2**: 0.795691
- **Variance**: 0.795889

These metrics indicate that the model is highly accurate and reliable, explaining approximately 79.57% of the variance in the dependent variable. This level of performance suggests that the model can effectively predict the energy content of recipes based on the input features.

When applied to ratios of training and testing data with a larger test portion, the 
RandomForestRegressor usually still outperformed others. 

## Limitations

While the RandomForestRegressor shows excellent training performance, its deep configuration and large number of estimators may pose challenges. The model might become computationally expensive and could potentially overfit if not properly validated on diverse datasets. Furthermore, its reliance on specific input features (food names and categories) limits its ability to account for other factors affecting energy content, such as preparation methods or ingredient combinations.

Please see the [datasheet](data_sheet.md "data sheet") for more detailed information on the dataset where various biases are discussed.

## Trade-offs

The choice to use a deeply configured RandomForestRegressor ensures high accuracy but at the expense of computational efficiency and potential overfitting. The high `max_depth` and number of trees allow the model to learn detailed data intricacies but may make it less adaptable to new, unseen data without similar depth in features. Moreover, the complexity of the model may reduce its interpretability, making it difficult for users to understand the basis of its predictions without substantial domain knowledge.

## Developer
- Adam de Zoete [(@zootle)](https://github.com/zootle "Adam de Zoete (@zootle)")

## Version
Last updated: April 2024