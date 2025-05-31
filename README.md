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