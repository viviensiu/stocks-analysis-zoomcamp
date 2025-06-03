**Link**
[Unit 2 repo for slides, recordings and notebook](https://github.com/DataTalksClub/stock-markets-analytics-zoomcamp/tree/main/02-dataframe-analysis)

**System Design View**
* Module 2 focuses on data processing, feature generation and merging datasets.

* Usually table data in webpages can be read using `pd.read_html` into Dataframe.
* However the preprocessing required are normally:
    * Cast columns into other data types.
    * Decide how to handle missing values or erroneous data (e.g. using regex).
    * Apply vectorised transformation for data processing: define new columns for transformed data.
    * Perform basic exploratory data analysis.
* [Pandas Time Series tutorial](https://pandas.pydata.org/docs/getting_started/intro_tutorials/09_timeseries.html): useful for processing stock analysis data.
* When processing time series data, think about the data type and the values you want to extract. Usually `pd.to_datetime()` is sufficient to convert strings to datetime values.
* You could use `timedelta` for time differences, e.g. durations.
* Interpolation (ffill, bfill) can be used to fill missing values, as some models are sensitive to missing values.
* Some errors might happen due to conversion issues, if you want to ignore errors, look into `errors=coerce` options when fill in missing values.
* Shift/lag can be used to calculate differences or percentage changes, create rolling windows, align time series,  creating lagged features, explore temporal dependencies on past values, build autoregressive models.
* **Macro Indicators** are useful data as markets are interconnected, often our models are restricted to features for a specific country, hence they could be good global data to enrich your analysis:
    * **VIX**: Volatility indicator. If values are high, it signals big market changes. This could mean a time when investors should start hedging. Hedging is a risk management strategy to offset potential losses by taking an opposite position, i.e. buying insurance against market fluctuations.
    * **Gold**: A safe haven asset. Gold price fluctuations may indicate people redistributing their assets into gold due to uncertainty towards the market.
    * **Oil** (Brent, WTI): Brent crude is a globally traded benchmark for pricing crude oil.
    * **Bitcoin**: reaching all time high at the moment.
    * Euro Area Yielf Curves: Defined by European Central Bank to represent the relationship between market remuneration rates and remaining time to maturity of debt securities. It tells you whether interest rates are expected to rise or fall in the future by its shape.
* Fundamental Indicators for traditional ratio analysis:
    * Used to pretict enterprise value or the fair value of a stock.
    * EPS (earnings per share) estimate: estimated before earnings announced.
    * EPS actual: actual earnings announced.
    * By looking at earnings announcement dates, you can see the trading volume fluctuations around that time.
    * Others such as revenue, net income, profit and loss (from financial reports), EBITDA.
* One could try to use all these indicators into your ML model and check if these metrics are important for your predictions.

**Creating unified dataset**
* Candlestick chart: financial visualisation of OHLCV data. Useful to represent time trends to view bullish vs bearish days.
* You can use the candlestick chart to calculate Simple Moving Average (SMA) for 10 and 20 days. It looks at the close price for last 10 and 20 days and is sensitive to changes over recent days, which SMA10 is more sensitive. So when SMA10 grows faster than SMA20 and they intersect, it signals down trend and that might be time to buy. When SMA10 intersects SMA20 from the bottom then it's uptrend and time to sell.
* Some advice on what we want to predict:
    * Historical growth is the main memory of OHLCV dataset to be used as a feature for future growth prediction. Closing prices should not be used as they may always be growing (non-stationary). Data used for training vs test/validation shouldn't be too different, there would be problem if if train using low values of Close and try to predict high values later on . * Historical growth is stationary and distributed around 1.   

**References:**
* [StockAnalysis.com](https://stockanalysis.com/): Good source for stock analysis data.