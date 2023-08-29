### Store Sales Forecasting

Alexis Cook, DanB, inversion, Ryan Holbrook. (2021). Store Sales - Time Series Forecasting. Kaggle. https://kaggle.com/competitions/store-sales-time-series-forecasting

**Author: Shaharyar Shaikh

#### Executive summary

The competition is to Forecast store sales on data from Corporación Favorita, a large Ecuadorian-based grocery retailer. 

Three methods were used to forecast sales (FB Prophet, Random Forrest Regression and XGBoost Regression). 

Exploratory data analysis gave the following insights:
- Highest average daily sales are in December and lowest in February
- There is a spike around the 15th and the 1st/last day of the month since that's when salary are paid
- Weekends have the highest sales since that's when most likely foot traffic is highest with Thursday having the lowest sales
- Sales over a longer period of time have a high negative correlation with oil prices (Peasrson's R: -0.77, pvalue statistically significant )


RMSE was used to validate the accuracy and XGBoost significantly outperformed the other 2 methods. 


#### Rationale
Forecasting inventory is critical for retailers. Having too much inventory takes up useful shelf space and produce can go bad. Having too less inventory can mean a loss of sale and customer. Inventory supply chain is complex and retailers have to place orders with suppliers several months in advance so the cost of under or over ordering can be staggering

#### Research Question
Can machine learning be used to forecast sales for a large retailer with multiple stores across the country that sell items across 30+ categories that are often on promotion. 

#### Data Sources
I plan to use a Kaggle competition as a capstone project. 
https://www.kaggle.com/competitions/store-sales-time-series-forecasting/overview


#### Methodology
Three main methods were used
- Facebook Prophet
- Random Forest Regression
- XGBoost Regression

#### Results

Prophet Model RMSE on Training set: 1052.09
RFR RMSE on Training set: 923.51
XGBR RMSE on Training set: 578.40

RFR RMSE on Validation set: 918.96
XGBR RMSE on Validation set: 565.24

I had to limit my GridSearch due to computational limitations. Best parameters 
RFR: {'max_depth': 5, 'max_features': 'sqrt', 'n_estimators': 15}
XGBR: {'eta': 0.1, 'max_depth': 5, 'n_estimators': 15}

XGBR performed really well but took a very long time to fit. Its mean fit time was 90.71 secs vs 17.88 secs for RFR.


#### Next steps
As a next step I will try to further tune the hyper parameters using google colab since I was limited by computational power on my personal computer. I was not able to make much use of calculated fields such as average selling price and if there is any impact of promotions that are being run in a store on stores that are located near by. 

#### Outline of project

https://github.com/sgshaikh/StoreSales_TimeSeriesForecasting


##### Contact and Further Information
Shaharyar Shaikh (sgshaikh@gmail.com)