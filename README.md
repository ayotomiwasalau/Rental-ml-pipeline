# Build an ML Pipeline for Short-Term Rental Prices in NYC.

This project is about building a reproducible ML pipeline with MLflow and Weight and Biases. 
A fictional properties company has a model that estimate the typical price for a given property based on the price of similar properties. 
they receives new data in bulk every week about properties prices, the model needs to be retrained with the same cadence, it requires an end-to-end pipeline that can be reused. It is basically to automate retraining of a machine learning model.

-- To run all the steps at once.
```bash
mlflow run  .

```

-- Each step can be run individually or you can specify some custom parameter value outside the config file

```bash
mlflow run . -P steps=download,basic_cleaning

mlflow run . \
  -P steps=download,basic_cleaning \
  -P hydra_options="modeling.random_forest.n_estimators=10 etl.min_price=50"
```


Vist [blog](https://ayotomiwasalau.com/) for full details.