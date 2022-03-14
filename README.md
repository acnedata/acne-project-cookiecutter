```
YYYYMM-client-project     <- The top-level repository in the stated naming convention.
│                            (e.g. 202203-acne-survey-analysis)
│
├── .dvc                  <- Configuration files for DVC.
│   ├── .gitignore
│   └── config
├── .gitignore            <- Set up with sensible defaults for excluding files.
│
├── .pre-commit.yaml      <- Configuration file for pre-commit.
│
├── CHANGELOG.md          <- Document to keep track of changes made to the project.
│
├── README.md             <- The top-level README with a brief description of this project.
│
├── data                  <- Here all data is stored which is being version controlled by DVC.
│
│   ├── interim           <- Data generated in intermediate cleaning and transformation steps.
│
│   ├── processed         <- The final, fully processed data used for traning and visualizations.
│
│   └── raw               <- The original, immutable data.
│
├── notebooks             <- Jupyter notebooks used for data exploration and code experimentation.
│                            Naming convention is MMdd-initials-description. (e.g. 0311-iw-data exploration)
│
├── pyproject.toml        <- Here are all project dependencies listed.
│
├── src                   <- Source code used in this project
│   └── __init__.py
└── tests                 <- Code for pytest.
    └── __init__.py
```
