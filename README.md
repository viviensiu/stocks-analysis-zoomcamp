# stocks-analysis-zoomcamp
My learning notes for DataTalks.Club Stocks Analysis zoomcamp.

**Disclaimer**: I do not use this course as a method for making investments, my main purpose is to understand what and how machine learning methods are used in stock market analysis from an investor who actually does so, and the reasons/justifications for doing so.

**Environment Setup for Mac**
```bash
conda create -n stocks-analysis-env
conda activate stocks-analysis-env
conda install numpy pandas yfinance notebook
conda install pandas-datareader plotly_express
conda install matplotlib
```

**Saving env for replication**
```bash
conda env export --from-history > environment.yml
```

**Alternative environment**
* Google Colab

**Cheat Sheet for Data Selection in Your Project**
* Select a market or country.
* Choose benchmarks for comparison, e.g. indexes and/or asset classes.
* Select macroeconomic indicators (global or regional).
* Dataset size: How many tickets/companies to include, what time period and history do you need? E.g. 25 years of data.
* Fundamental data: Do you need company fundamentals? e.g. YFinance provides 4 years of data.
* Financial reporting and alternative data.
* Important: Do not leak data! You must only use data up to the prediction date, never use future data in your model or analysis!
* Also, start early as majority of the work would be on collecting and consolidating data.
