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

# Grading

- Motivation [2pts]: What problem are you tackling? Why is it interesting? A non-specialist audience should be able to understand why your work is interesting. What type of project will this be (novel methods development, application to novel dataset, detailed benchmarking/analysis on existing dataset, theory)?
  - [-1] Motivation is missing crucial details about the choice of problem and why it's interesting
  - [-1] Significant issues with presentation clarity
  - [-2] Motivation is missing entirely
- Context [3pts]: Explain how you build upon previous work and how your results compare to what has been done previously. Provide background needed for a general scientific audience to understand the methods you will introduce next (e.g., provide a background in biology if needed).
  - [-1] Context is missing important reference to very significant previous work
  - [-1] Missing background needed by non-specialists to understand subsequent methods development and analysis
  - [-1] Issues with presentation clarity
  - [-3] Context is missing entirely
- Method [5pts]: Describe the methods that you are using. For experimental projects, describe the algorithms (SVM, PCA, etc.). If you use existing methods, you don't need to redefine them from scratch, but make sure that a reader who took the course can understand what you're planning to do. If you propose novel methods, make sure to provide enough detail and context. For theory projects, state the results you are going to establish. Justify your choice of methods.
  - [-1] Missing minor details in the methods' definition
  - [-2] Missing major details in the methods' definition
  - [-1] Minor issues / correctness errors in justifying choice of methods
  - [-2] Justification for the chosen methods is missing entirely or has major issues
  - [-1] Minor issues with methods' novelty (for novel method development projects only)
  - [-2] Major issues with methods' novelty (for novel method development projects only)
  - [-1] Minor issues with presentation clarity
  - [-2] Major issues with presentation clarity
  - [-5] Method is missing entirely
- Setup [5pts]: Describe how you apply the methods. For experimental projects, define the experiments that you've run; readers should be able to reproduce your results with a reasonable amount of effort. Consider including datasets, metrics, data splits, features, hyper-parameter selection process,  learning rates, number of epochs used, etc. For theory projects, state your assumptions, state any lemmas you are using (and cite references), and define your symbols. Justify your choices.
  - [-1] Missing minor details in the definition of the setup
  - [-2] Missing major details in the definition of the setup
  - [-1] Minor issues / correctness errors in justifying choice of setup
  - [-2] Justification for the proposed setup is missing entirely
  - [-1] Minor issues with novelty of the dataset setup (e.g., very similar to an existing popular dataset/benchmark/Kaggle competition; only for projects that focus on novel datasets)
  - [-2] Major issues with novelty of the dataset setup (e.g., corresponds to an existing popular dataset/benchmark; only for projects that focus on novel datasets)
  - [-1] Minor issues with presentation clarity
  - [-2] Major issues with presentation clarity
  - [-5] Setup is missing entirely
- Outcomes and Results [10pts]. Describe and explain the outcomes of applying the methods. For experimental projects, make sure to describe and analyze the results of your experiments. Consider including: train/test performance, learning curves, model samples, error analyses, ablation analyses, etc. Most projects should also include results from baselines. If you're analyzing/benchmarking non-novel methods on existing datasets, you should provide details about how you tuned your methods to improve performance. For theory projects, formally prove your theorems. Comment and discuss the outcomes of your work.
  - [-1] Missing minor details in the definition of the outcomes
  - [-2] Missing moderately important details in the definition of the outcomes
  - [-3] Missing major details in the definition of the outcomes
  - [-1] Minor issues / correctness errors in discussing the outcomes
  - [-2] Major issues / correctness errors in discussing the outcomes
  - [-3] Discussion of the outcomes is missing entirely
  - [-1] Minor issues with novelty and depth of method tuning (only for projects that focus on benchmarking/analysis)
  - [-2] Medium issues with novelty and depth of method tuning (only for projects that focus on benchmarking/analysis)
  - [-3] Major issues with novelty and depth of method tuning (only for projects that focus on benchmarking/analysis)
  - [-1] Minor issues with presentation clarity
  - [-2] Medium-level issues with presentation clarity
  - [-3] Major issues with presentation clarity
