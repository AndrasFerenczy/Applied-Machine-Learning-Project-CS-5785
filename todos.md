# TODOs

Overleaf:
- Email: outfits_cork.28@icloud.com
- Password: noxnir-hutJoq-8pirky
- Link: https://www.overleaf.com/9571526225tpzymjtfvbws#559892

1) Better preprocessing (Karan):
    - How should the NaN values be handled for XGBoost (`training_v2.ipynb`, Cell 1)? Right now, the model takes the average of that column and uses it for NaN values.
        - Possible solutions: take the median or other calculated number instead?
        - Compute it based on the row, not the column? More precisely, compute it using the previous days-to-departure numbers (and e.g.: calculate the mean from those)?
    - Any missing features which would be useful for achieving a better model?
    - Should the values of calculated from the flight date be normalized (e.g.: between 0 and 1): `'day_of_month'`, `'is_weekend'`, `'is_public_holiday'`, `'days_from_summer_start'` to achieve a better performance?

2) Better training (Brandon):
    - A gridsearch would be useful to determine what hyperparameters to use (`max_depth, learning_rate, n_estimators, subsample, colsample_bytree, objective='reg:squarederror'`)
    - The different models created by gridsearch and their performance should be plotted in various ways, because that would be really nice to show in our write-up. (e.g.: how does the model's performance converge with different le arning rate, number of tree's, etc.)
    - When the hyperparameters are tuned to the best version, a final task is to test it on the `test` set, as this set is reserved to be used only at the very end.
    - Kuleshov's slides about evaluation can be helpful (https://github.com/kuleshov/cornell-cs5785-2025-applied-ml/blob/main/slides/lecture23-evaluation-tools.ipynb)

- Document overview:
    1. Select a nice Latex template on overleaf we can use (Andras)
    2. Configure it for the AML Write-Up (Andras)

    3. Abstract (created at the end)
    4. Introduction (Andras)
        - Problem statement
        - Solution 
    5. Data Used (Expedia dataset)
        - Preprocessing steps
    6. Model description of XGBoost
    7. Benchmarking metrics used
        - e.g.: MAE
    8. Experiments
        - Training variations and outcomes
        - One or two concrete examples to make it precise       
    3. Conclusion (created at the end)

