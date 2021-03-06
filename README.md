# Random-Forest-Algorithm-for-Predicting-Stock-Market-Trend
Applying SVM to the Financial Markets to uncover key insights for Investment

The stock market data for S&P500 was extracted from Yahoo Finance from Jan 1, 2011 to 30 June, 2018. The raw data consisted of Open, High, Low and Close Prices and Volume.

Data Processing: 4 Distinct Technical Indicators were genenerated from the price data using the quantmod package. The change in value of the each indicator with respect to the previous period was then calculated.

Predicted Variable: The change in the Close Price was taken as proxy for Price Trend. If Close Price for next day is higher than the Closing Price of the previous day, then the trend is set to +1 else its set to 0. The dataset was then cleansed from dates for which at least a part of the data was missing.

Assumption: The probability of the close prices for 2 consequtive periods of being equal is very low or 0 from my observation. Hence, I ignored that condition.

Training the Model:

The data was then split into training and test data based on 80-20 split. All the quantitative data was then scaled. The Price trend for the next month was then predicted from the scaled inputs from the 4 indicators. The model was trained on the training set.

The model gave a 54% predictive accuracy on the test data set.


Data Source: 

https://finance.yahoo.com/quote/%5EGSPC/history?period1=1293858000&period2=1530331200&interval=1d&filter=history&frequency=1d
