# Time-Series-Forecasting-with-Prophet-
Forecast time series data using the Prophet library by Facebook.
from fbprophet import Prophet

# Assume you have a DataFrame 'df' with time series data
# Prepare the DataFrame with 'ds' (datestamp) and 'y' (value) columns

model = Prophet()
model.fit(df)

future = model.make_future_dataframe(periods=365)  # Forecast for the next year
forecast = model.predict(future)

# Access and visualize the forecast
