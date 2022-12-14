# S-P500_price_prediction
S&amp;P500 consists of the 500 largest companies listed on exchanges in the United States. 
I will try to predict S&P500 stock price +20 working days into the future using: feature engineering and feature selection.

### Timeframe: 
- '1993-01-29' until '2022-12-12'

### Prediction target: 
- +20 days 

### Work methods:
- Creation of new input features from existing features.
- Importing features of economic activity indicators with correlativity to the stock market from FRED.
- Filling sparse data using interpolation.
- Data transformation.
- Train, test, validation split: 80-10-10
- Automated features selection.

### Goal:
- Beat the benchmark model.

## Results:
### Feature creation:
- 17 features imported, 5 selected for the final model
- 29 features created, 20 selected for the final model

### Imported features selected:
- 'money_supply' 
- 'consumer_sentiment' 
- 'net_migration' 
- 'usa_pop' 
- 'world_pop'

### Model:
- Selected model: ElasticNet() with validation MAPE of: 3.43
- Features transformation decreased validation MAPE to: 2.69
- Features selection decreased validation MAPE to: 2.16

### Benchmark:
- LinearRegression() with single feature 'adj_close', test MAPE of: 2.522

### Final model:
- ElasticNet() + selected features + transformation test MAPE of: 2.506

Conclusion:
- Up to 2.5% of the real stock price can be predicted 20 working days in advance using the model



