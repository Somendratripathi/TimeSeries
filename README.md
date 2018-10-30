"A 4 day challenge to come up with accurate forecasts for 10K time series" 


Summary

A series of dives into each of the 5 files were made in an attempt to extract patterns that explain the 10,000 product’s time-series. OOS flags were used to remove the impact of OOS on the sales, for accurate predictions it is assumed that the product inventory will be well optimized and 0 products will be out of stock in future. The solution also assumes that promotion start dates are known in advance in future and includes promo related features for prediction (Promo related attributes other than the start—date are yet to be explored). 

XGboost and tslm are trained and tested on the dataset achieving 20.7 and 20 RMSE respectively. XGBoost was trained on only 10% of the train cases and tuning was limited to a subset of the hyperparameter space, releasing the constraints would lead to immediate improvement of the results. 

Ensembling both the approaches is proposed as the immediate next step. This may improve accuracies by overcoming XGBoost’s inability to extrapolate. Additionally, other approaches are discussed in the ‘Future Steps’ section.

The following document discusses the solution in brief along with approaches considered and justifications to why they were used. 

Also, included is the .ipynb that aims to walk you through the following: 
1.	Exploratory analysis and visualizations to assess the impact of seasonality, trend, missing values, out of stock, and promos.
2.	Feature building engineering process
3.	Reproducible code for the forecasting tool
