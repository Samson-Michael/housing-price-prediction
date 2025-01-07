# Housing Price Prediction
### Project Overview
This Python-based machine learning project predicts housing prices by analyzing past data and key features like house size. The goal is to provide accurate forecasts for prices of residential properties.

# Data Sources
This dataset is sourced from the following:

https://www.kaggle.com/datasets/harishkumardatalab/housing-price-prediction/data

# Tools Used for this project

This analysis utilized the following Python libraries:
- Libraries: NumPy, Pandas, Seaborn, Matplotlib
- Metrics: Mean Absolute Error
- Encoding: OneHotEncoder
- Preprocessing & Models: StandardScaler, SimpleImputer, SVR, RandomForestRegressor, GridSearchCV

# Data Cleaning/Preparation

- Missing values were detected and filled using proportional methods.
  
- Outliers were identified and trimmed to ensure data integrity.

# Exploratory Analysis
![image](https://github.com/user-attachments/assets/d5fcfd74-8707-4eb1-8d54-8a158b8b46ce)

The histograms visualize the distribution of categorical features in a dataset related to house listings, revealing insights into factors like location preferences, amenities, and property characteristics.

![image](https://github.com/user-attachments/assets/aaa69848-f9c6-41bf-b7f9-4ea6c9cfcf0e)

Most houses are located near main roads, lack guest rooms and basements, and are situated in preferred areas with features like air conditioning and hot water heating. Furnished houses with 2-3 bedrooms, 2 bathrooms, 2 stories, and 1 parking space are the most common.

![image](https://github.com/user-attachments/assets/af5a7965-2440-46ca-8da9-981c4f357857)

The pairplot reveals that price is strongly correlated with area and moderately correlated with the number of bedrooms and bathrooms. Other features like stories and parking spaces seem to have weaker relationships with price.

# Predictive Analysis

## Baseline Model Evaluation

- Mean Apartment Price: ₦4,045,012.33
  
- Baseline MAE (Mean Absolute Error): ₦973,692.83
  
Using the average apartment price as the baseline prediction, the error suggests that predictions based solely on the mean would be off by nearly ₦1 million on average. This serves as the benchmark against which advanced models are compared. Any model with an MAE lower than this value would demonstrate improved predictive capability.

## Random Forest Regressor Performance

- Random Forest MAE: ₦252,936.94
  
The Random Forest Regressor performed significantly better than the baseline, reducing the MAE by approximately 74%. This demonstrates the model's ability to generalize well and capture complex relationships in the data. Its lower error makes it a strong candidate for predicting housing prices.

# Hyperparameter Tuning and Performance

### Best Parameters (Grid Search)

- max_depth: 15
  
- max_features: sqrt

- min_samples_leaf: 2

- min_samples_split: 5

- n_estimators: 100

- Best MSE (Mean Squared Error): 918,525.47
  
The hyperparameter tuning process used Grid Search to optimize the Random Forest Regressor. This resulted in a model with improved performance by reducing overfitting and enhancing generalization.

# Hyperparameter Tuning
![image](https://github.com/user-attachments/assets/c5cc17d4-3e86-43c4-99ff-90b2722330dc)

This plot shows the most important factors for the model to predict house prices. House size is the top factor, as expected. Interestingly, unfurnished houses seem to have a significant impact on the model's predictions. The number of bedrooms and parking spaces also play a major role in price estimation


# Conclusion

This housing price prediction project successfully utilized machine learning techniques to predict property prices with high accuracy. The Random Forest Regressor, after hyperparameter tuning, significantly outperformed the baseline model with a 74% reduction in error (MAE of ₦252,936.94 vs. ₦973,692.83).


Key features like house size, furnishing status, and the number of bedrooms were identified as critical drivers of price. These insights guides stakeholders in the housing market to make decisions about property pricing, marketing strategies, and renovation priorities.


Moving forward, integrating this model into a dynamic pricing tool and refining it with larger, updated datasets will ensure its continued relevance and impact. This project not only demonstrates the power of machine learning in solving real-world problems but also lays a solid foundation for further advancements in the real estate sector.
