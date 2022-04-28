![](prophet_plotly.png)
# Forecasting_Net_Prophet
As a Solutions Analyst at MercadoLibre. With over 200 million users, MercadoLibre is the most popular e-commerce site in Latin America. Tasked with analyzing the company's financial and user data in clever ways to help the company grow, we apply forecasting models as a solution. To find out if the ability to predict search traffic can translate into the ability to successfully trade the stock, an analysis will highlight growth opportunities.
In a bid to drive revenue,we have produced a Jupyter notebook that contains data preparation, analysis, and visualizations for all the time series data that the company needs to understand.The use of text and comments to document your findings are included in the code. The notebook contains the following:


Visual depictions of seasonality (as measured by Google Search traffic) that are of interest to the company.


An evaluation of how the company stock price correlates to its Google Search traffic.


A Prophet forecast model that can predict hourly user search traffic.


Answers to the questions in the instructions that you write in your Jupyter notebook.


A plot of a forecast for the company’s future revenue.


You’ll gain proficiency in the following tasks:


Identifying patterns in time series data.


Mining for patterns in seasonality by using visualizations.


Building sales-forecast and user-interest predictive models.


Step 1: Found unusual patterns in hourly Google search traffic.


Step 2: Mined the search traffic data for seasonality.


Step 3: Related the search traffic to stock price patterns.


Step 4: Creatde a time series model by using Prophet.


Step 5: Forecasted the revenue by using time series models.


Found Unusual Patterns in Hourly Google Search Traffic

Sliced the data to just the month of May 2020. (During this month, MercadoLibre released its quarterly financial results.) Used hvPlot to visualize the results. 


Calculated the total search traffic for the month, and then compared the value to the monthly median across all months. 

Mined the Search Traffic Data for Seasonality

Marketing realizes that they can use the hourly search data, too. If they can track and predict interest in the company and its platform for any time of day, they can focus their marketing efforts around the times that have the most traffic. This will get a greater return on investment (ROI) from their marketing budget.
To that end, I mined the search traffic data for predictable seasonal patterns of interest in the company.


Grouped the hourly search data to plot the average traffic by the day of the week (for example, Monday vs. Friday).


Using hvPlot, visualized this traffic as a heatmap, referencing index.hour for the x-axis and index.dayofweek for the y-axis. 


Grouped the search data by the week of the year. 


Related the Search Traffic to Stock Price Patterns

During a meeting with people in the finance group at the company, I mentioned my work on the search traffic data. They wanted to know if any relationship between the search data and the company stock price exists, and if I can investigate.

To do so, I complete the following steps:


Read in and plot the stock price data. Concatenated the stock price data to the search data in a single DataFrame.


Noted that market events emerged during 2020 that many companies found difficult. But after the initial shock to global financial markets, new customers and revenue increased for e-commerce platforms. So, I sliced the data to just the first half of 2020 (2020-01 to 2020-06 in the DataFrame), and then used hvPlot to plot the data.


Created a new column in the DataFrame named “Lagged Search Trends” that offsets, or shifts, the search traffic by one hour. Created two additional columns:


“Stock Volatility”, which holds an exponentially weighted four-hour rolling average of the company’s stock volatility


“Hourly Stock Return”, which holds the percentage of change in the company stock price on an hourly basis




Reviewed the time series correlation, and then answered the following question: Does a predictable relationship exist between the lagged search traffic and the stock volatility or between the lagged search traffic and the stock price returns?



Step 4: Created a Time Series Model by Using Prophet

Set up the Google search data for a Prophet forecasting model.


After estimating the model, plotted the forecast. 


Plotted the individual time series components of the model to answer the following questions:


What time of day exhibits the greatest popularity?


Which day of the week gets the most search traffic?


What's the lowest point for search traffic in the calendar year?
