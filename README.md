# Predicting-seasurface-temperatures
Comparing all 3 models, using the Residual Mean Squared Error as our metric,  we see that the BSTS model performs the best with the lowest RMSE score.  We suspect that the Bayesian approach worked so well because it can infer causal impacts within time series. In this case, whether 1 or more layers greatly influenced the temperatures of the layers beneath it. In our coefficient analysis for a model size of 1 we confirmed this was the case.  


We faced a few issues in this project. For the SARIMA models, we started out with a trial and error method to determine the order of the seasonal model required to fit the data. This method proved difficult since there are numerous combinations of numbers that could have made the model. Reading the ACF and PACF model and using that as a guide resulted in producing the best model we have provided above.  

Another issue we ran into was trying to configure the predict method to work with our data. The predict method produced predictions for the entire dataset instead of just future data. Using the one step ahead prediction and the forecast function was able to rectify this error.
