**Link**
[Unit 3 repo for slides, recordings and notebook](https://github.com/DataTalksClub/stock-markets-analytics-zoomcamp/tree/main/03-modeling)

* We begin by wrapping up creating a unified dataset from multiple sources:
    * Define variable sets
    * Create dummy variables for categorical data. e.g. one-hot encoding.
    * Performing correlation analysis.
    * Apply temporal split.
* The primary key is a pair <Date, Ticker> with other features to predict future growth.
* Key feature categories:
    * TO_PREDICT: Never include as features in model as these are for predictions (else data leakage).
        * `is_positiive_grwoth_future_{i}d`
        * `growth_future_{i}d`
    * TO_DROP: Not to be used as features but may be useful later.
        * Year, Date, Index, Quarter.
        * OHLCV
        * CATEGORICAL (non-textual)
    * NUMERICAL: All features used.
* Key assumptions:
    * Independent observations, although this is simplification since there is dep between tickers and time.
    * Some advanced models may require a different data organisation, e.g. Graph Neural Network have edges with relationship, or a feature can be an array.
* In correlation analysis, 
    * Pay attention to the indices used. E.g. if we are using indices such as for Bonds, and we are predicting stocks growth, bonds indices would be weakly correlated to it since it may not reflect similar volatility.
    * Weak individual features may be combined to provide better correlations.
    * Seek to increase features for better generalisation of the model.
    * Use ML model explainability to understand which metrics are most improtant and ientify additional features to include.
