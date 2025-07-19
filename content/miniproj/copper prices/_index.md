---
title: Prediction of Future Copper Prices
date: 2025-07-19
author: Mini Project 3
---
---
### Overview:
The goal of this project was to build a model that predicts the ever-fluctuating price of copper in the three major copper future exchanges: Shanghai Futures Exchange (SHFE), London Metal Exchange (LME), and CME Group / COMEX Copper (HG). 

### Data Cleaning:
All three datasets containing historical prices of copper at the three major exchanges were converted into a data frame format and put into a standardized form before further processing by erasing index labels. For clarity purposes, the number of rows and columns for each dataset was obtained as well.

### Exploratory Data Analysis (EDA):

#### Plot 1:
<img width="576" height="453" alt="1" src="https://github.com/user-attachments/assets/6e970c63-1649-43e3-8e6f-8745e08f9055" />
To better understand the training data which would be used to train a model for prediction of future copper prices, the graph above that depicts fluctuating copper prices across all three exchanges from 2010-present was created and analyzed. This graph shows that the LME and COMEX price trends follow a relatively similar price trend-line while the SHFE trend line has shallower troughs and much higher peaks. While this could reveal that the Chinese markets have a lower volatility, the copper prices drop by roughly the same amount, indicating not a lower volatility, but simply a higher starting price.

#### Plot 2:
<img width="567" height="453" alt="2" src="https://github.com/user-attachments/assets/d2a9b840-7553-4d2b-ae96-4f2c2b92198f" />
The monthly average price of copper in each of the three major copper exchanges was plotted in a line graph across a one-year period. After analysis of this plot, it can be seen that the line depicting the Shanghai Futures Exchange is significantly higher than that of LME and COMEX. This difference suggests that China’s copper market could be especially influenced by local demands or trading policies. 

### Modeling:

#### Model 1: Model Selection Based on Estimator Count 
<img width="585" height="432" alt="3" src="https://github.com/user-attachments/assets/1bebae37-edee-415a-bad2-df6f48efb0c2" />
Multiple Random Forest models were trained and tested in order to determine which number of decision trees (estimators) would minimize the Root Mean Square Error (RMSE) for a final model. Each Random Forest model differed in the number of trees tested to evaluate if increasing the number of trees would improve the model’s accuracy. As a lower RMSE indicates better predictive accuracy and smaller error, the plot shows that RMSE reaches its minimum at 150 trees, making it the most optimal choice for Model 2.

#### Model 2: The Final Model
<img width="1002" height="545" alt="4" src="https://github.com/user-attachments/assets/cc981e87-34ce-4e46-9663-3d7eb432c359" />
Based on Model 1, 150 decision trees was used in Model 2 (a single Random Forest model) as this number minimized RMSE. The blue line in Model 2 depicts the actual historical copper prices from 2010-mid 2025 while the orange line depicts predicted copper prices based on forecasting done by the model. The model appears to have high accuracy as the orange line (predicted prices) closely follows the blue line (historical prices), indicating a strong performance.
