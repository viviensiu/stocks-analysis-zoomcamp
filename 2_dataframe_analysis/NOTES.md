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
    * 

**References:**
* [StockAnalysis.com](https://stockanalysis.com/): Good source for stock analysis data.