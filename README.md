![Predicting Energy Intake from Recipe Ingredients](assets/images/github-header.png "Predicting Energy Intake from Recipe Ingredients")

# Predicting Energy Intake from Recipe Ingredients

## Project Overview

This project aims to investigate the feasibility of machine learning in 
effectively predicting the energy, or calorie content, of ingredients used in recipes. Every year 
millions of people are affected by health conditions related to diet and nutrition. Research show that it is often a struggle to 
access the right information to make informed decisions about their food choices. There are many 
industries who are reliant on providing accurate nutritional information to consumers, yet this 
is not always available due to the complexity of food composition and preparation.

Overall, a 78% accuracy has been achieved on predicting the calorie content, Energy (kJ) / per 
100g, of food ingredient on a broad set of 2893 food ingredients. This is a significant step forward in 
achieving wider goals of predicting a broader spectrum of nutritional attributes.

The project consists of a [Jupyter notebook](notebook.ipynb "Jupyter notebook"), [model card](model_card.md "model card") and 
[datasheet](data_sheet.md "data sheet"). The original dataset is provided alongside the permutations used for the project.

## Rationale

The use of machine learning for the application of nutritional prediction in both personal and 
commercial settings can have far-reaching benefits:

- **Dietary Management and Nutrition**: For individuals tracking their caloric intake for 
   weight management or health conditions such as diabetes, accurate information on calorie 
   content can help in making informed dietary choices. This can assist in maintaining or 
   achieving a balanced diet.

- **Labelling and Packaging**: Accurate calorie predictions can aid food manufacturers in 
   providing precise nutritional information on packaging, which is crucial for consumer 
   transparency and regulatory compliance.

- **Food Service Application**: Chefs and food service professionals can use calorie content 
   predictions to design meals that meet specific nutritional criteria, which is especially 
   useful in settings like hospitals, schools, and health-focused restaurants and supermarkets.

- **Food Technology**: Integrating calorie prediction algorithms into apps and devices can 
   enhance the functionality of kitchen gadgets and fitness trackers, making them more useful 
   for consumers aiming to monitor their overall fitness and health.

- **Research and Development**: For researchers focusing on food science and human nutrition, 
   understanding the caloric content can help in studying the impacts of various foods on human 
   health and in developing new food products that fit into healthier lifestyle choices.

- **Personalized Nutrition**: With advances in personalized medicine, predicting calorie 
   content can be part of broader efforts to tailor diets to individual genetic profiles, 
   lifestyle factors, and health goals.

- **Reducing Food Waste**: Knowing the caloric value of ingredients can also aid in better 
   managing food resources, planning meals more efficiently, and reducing waste by utilising 
   ingredients appropriately according to dietary needs.

Overall, the ability to predict calorie content accurately can contribute significantly to 
health and wellness, culinary practices, consumer technology, and broader scientific research.

Assistive technology such as this can be used to improve the health conditions of many around 
the world and this project simply scratches the surface of the potential use of machine 
learning in the field of nutrition.

## Research

The research undertaken to form the basis of this project is wholly inspirational. Since the 1940's 
nutritional data has been collected on food ingredients and their composition by the science 
community, resulting in a highly detailed dataset which only this project hardly scratches the 
surface of. This has been compiled and maintained by government bodies many years now. Please 
review the [datasheet](data_sheet.md "data sheet") for more detailed information.

## Data Sources and Content

The dataset used for this analysis is the 'McCance and Widdowson’s The Composition of Foods 
Integrated Dataset 2021' and is provided by Public Health England. It contains detailed 
nutritional information for 2889 ingredients across 14 product categories. The dataset includes categorical 
data and scientific nutrient composition for each ingredient, making it highly suitable for 
practical application including machine learning models to predict nutritional value.

The data is sourced from [Public Health England](https://www.gov.uk/government/publications/composition-of-foods-integrated-dataset-cofid "Public Health England"), 
featuring 
ingredients 
that have undergone significant testing due to changes in food composition driven by new farming 
and manufacturing practices, public health initiatives, and variations in preparation and cooking methods.

Please see this [datasheet](data_sheet.md "data sheet") for more detailed information on the dataset and the 
elements used within this project.

## Methodology

The project is broken down into the following steps:

1. Obtaining the data set for the analysis 
2. Exploration, cleaning and pre-process the data 
3. Dimension reduction and feature engineering 
4. Determine the machine learning task 
5. Partition the data 
6. Choosing the machine learning techniques 
7. Training the models and using on a test dataset 
8. Interpreting the results 
9. Deploying in a sample technique

During the data pre-processing phase, I have vectorized words associated with food names and groups 
to make them more generalizable to a broader spectrum of targets. The aim of this project was to develop a machine learning model capable of adapting to a wide range of recipes and ingredients, thereby reducing its specificity to unseen data. The implementation details are shown below.

![Word Cloud of Ingredients](assets/images/food-composition-word-cloud.png "Word Cloud of Ingredients")

## Model evaluation

Many supervised machine learning models have been considered for this project, including:

- Principal Component Analysis (PCA) with Linear Regression
- Ridge Regression
- Regression using LightGBM
- Partical Least Squares Regression with ReLU Activation
- Random Forest Regressor
- XGBoost for Regression
- Support Vector Regression with and without PCA
- K-Nearest Neighbours Regressor


During the experimental phase, I discovered that employing Principal Component Analysis (PCA) 
actually 
reduced accuracy due to the high specificity required by the data. Using Linear Regression alone yielded poor results. Surprisingly, even Support Vector Regression, typically lauded for its effectiveness in high-dimensional regression tasks, also underperformed. This led me to focus on six other models for more in-depth analysis.

## Hyperparameter Optimisation

The models were extensively hyperparameter tuned using Optuna to ensure the best possible 
parameter selection for choosing a suitable model. 

![Hyperparameter Optimisation with Optuna](assets/images/optuna-XGBRegressor-slices.png "Hyperparameter Optimisation with Optuna")

Various models such as LightGBM were very slow to train and optimise, but others could be run 
through hundreds of iterations to find the optimum parameters.

## Model results

The following models were evaluated using Mean Squared Error (MSE), Root Mean Squared Error (RMSE), R-squared (R2), and Variance:

|                       | Train Accuracy | Train RMSE |    MSE |    RMSE |       R2 |   Variance |
|:----------------------|---------------:|-----------:|-------:|--------:|---------:|-----------:|
| Ridge                 |       0.876325 |    221.559 | 131400 | 362.491 | 0.712666 |   0.714562 |
| LGBMRegressor         |       0.611449 |     392.71 | 178633 | 422.65  | 0.60938  |   0.610797 |
| PLSRegressionReLU     |       0.852259 |    242.157 | 131028 | 361.977 | 0.71348  |   0.716765 |
| RandomForestRegressor |       0.964799 |    118.202 | 114840 | 338.88  | 0.748878 |   0.748959 |
| XGBRegressor          |       0.995883 |    40.4259 | 100474 | 316.977 | 0.780291 |   0.780765 |
| KNeighborsRegressor   |       0.996474 |    37.4095 | 136899 | 369.999 | 0.70064  |   0.701494 |

The following finding as a result of the model evaluation:

- **Ridge Regression**: Decent R2 and variance, but higher RMSE and MSE compared to other models.
- **LGBMRegressor**: Good performance across all metrics, lower RMSE and MSE than Ridge, and decent R2.
- **PLSRegressionReLU**: Lower performance in accuracy and higher RMSE and MSE than some other models, though R2 and variance are reasonable.
- **RandomForestRegressor**: Excellent performance in terms of RMSE and MSE, and the highest R2 and variance, showing strong predictive power and consistency.
- **XGBRegressor**: Outstanding performance with the lowest RMSE and MSE, and the highest R2 and variance, suggesting excellent predictive accuracy and consistency.
- **KNeighborsRegressor**: Despite having the same high train accuracy and low RMSE as XGBRegressor, it has a significantly higher MSE and the lowest R2 and variance, indicating potential issues in generalizing.

The following graph shows the accuracy of the models:

![Model Accuracy Comparison](assets/images/model-accuracy-R2-scores.png "Model Accuracy Comparison")

Overall, there is a good level of accuracy over most of the models. The XGBoost for Regression model has stood out due to its high accuracy and low RMSE. If this overfits on further unseen data then the Random Forest Regressor would be the next best model to use.

Please see this [model card](model_card.md "model card") for more detailed information on the final 
model used within this project.

### Conclusion

This research project employs sophisticated machine learning techniques to predict the calorie 
content of various food ingredients, a crucial endeavour for nutrition management and public 
health. It has been proved feasible that machine learning could be practical for use in this 
field with scope to delve deeper into potential practical implementations.

Future work might include merging models and/or refining feature engineering to enhance predictions and expand the range of ingredients covered across a broader demographic. Additionally, there is potential to delve deeper into the data, improve word classification, and implement different tokenization methods, such as stemming and lemmatization, to interpret words in their contextual forms. These advancements could increase the model's applicability and accuracy.

### Author
- Adam de Zoete [(@zootle)](https://github.com/zootle "Adam de Zoete (@zootle)")

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE "license") file for 
details

