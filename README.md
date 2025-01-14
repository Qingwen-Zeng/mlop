# mlop

A short description of the project.

## Project structure

The directory structure of the project looks like this:
```txt
├── .github/                  # Github actions and dependabot
│   ├── dependabot.yaml
│   └── workflows/
│       └── tests.yaml
├── configs/                  # Configuration files
├── data/                     # Data directory
│   ├── processed
│   └── raw
├── dockerfiles/              # Dockerfiles
│   ├── api.Dockerfile
│   └── train.Dockerfile
├── docs/                     # Documentation
│   ├── mkdocs.yml
│   └── source/
│       └── index.md
├── models/                   # Trained models
├── notebooks/                # Jupyter notebooks
├── reports/                  # Reports
│   └── figures/
├── src/                      # Source code
│   ├── project_name/
│   │   ├── __init__.py
│   │   ├── api.py
│   │   ├── data.py
│   │   ├── evaluate.py
│   │   ├── models.py
│   │   ├── train.py
│   │   └── visualize.py
└── tests/                    # Tests
│   ├── __init__.py
│   ├── test_api.py
│   ├── test_data.py
│   └── test_model.py
├── .gitignore
├── .pre-commit-config.yaml
├── LICENSE
├── pyproject.toml            # Python project file
├── README.md                 # Project README
├── requirements.txt          # Project requirements
├── requirements_dev.txt      # Development requirements
└── tasks.py                  # Project tasks
```

- *data.py*: this file is responsible for everything related to the data. This includes loading, cleaning, and splitting the data. If the data needs to be pre-- processed then running this file should process raw data in the data/raw folder and save the processed data in the data/processed folder.
- *model.py*: this file contains one or model definitions.
- *train.py*: this file is responsible for training the model. It should import the training/validation data interface from data.py and the model definition from model.py.
- *evaluate.py*: this file is responsible for evaluating the model. It should import the test data interface from data.py and load the trained model from the models folder. Output should be performance metrics of the trained model.
- *api.py*: this file is responsible for serving the model. It should import the trained model from the models folder and provide an interface for making predictions.
- *visualize.py*: this file is responsible for visualizing the data and model. It should import the training/validation/ test data interface from data.py and the trained model from the models folder. Output should be visualizations of the data and model.

Created using [mlops_template](https://github.com/SkafteNicki/mlops_template),
a [cookiecutter template](https://github.com/cookiecutter/cookiecutter) for getting
started with Machine Learning Operations (MLOps).
