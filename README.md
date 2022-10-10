RecSys
==============================

Tooling for recommender systems implementation


Terminology
------------

**Collaboration-based recommendations** are based on user behavior. Assume I like content X and dislike content Y. To recommend content to me, we first find users similar to me (i.e., like X, dislike Y). Then, from those users, what are content they liked, but I’ve not seen? Those content are then recommended to me. With user behavioral data, users can (passively) “collaborate” to create recommendations for each other. Collaborative filtering is probably the most well-known approach.

**Content-based recommendations** are based on item metadata. Given the content I’ve seen (and clicked through), content-based recommenders suggest content of similar topic, location, sources, etc. Relative to collaboration-based recommenders, content-based recommenders tend to be more effective when the content is new and we don’t have enough user behavioral data about it yet (i.e., cold-start problem)

**Few words about ranking** 

Ranking can be framed as either a classification or learning to rank problem. As a classification problem, we can score candidates based on probability of click or purchase. Logistic regression with crossed features is simple to implement and a difficult baseline to beat. Decision trees are also commonly used. As a learning to rank problem, commonly used algorithms include XGBoost and LightGBM. 

Project Lifecycle challenges and opportunities
------------------
Browse the repo folders to find more about the challenges

1. Problem framing
3. Experimentation management
4. Model validation
5. Heuristics rules
6. Model card
7. Real-time Inference 
8. Online training

Awesome tools and resources
-----------------
### ML Libraries
- [LightFM](https://making.lyst.com/lightfm/docs/index.html): Lyst open source implementation of Matrix Factorization neural networks
- [Wide & Deep TensorFlow estimator](https://www.tensorflow.org/api_docs/python/tf/estimator/DNNLinearCombinedClassifier)

### Papers
- [LightFM paper](http://arxiv.org/abs/1507.08439)
- [Wide & Deep paper](https://arxiv.org/abs/1606.07792)

### Blog posts
- [Eugene Yan website](https://eugeneyan.com/): Amazing resources on practical recommender system implementation at scale
- [Wide & Deep docs from Google](https://ai.googleblog.com/2016/06/wide-deep-learning-better-together-with.html)

Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------
