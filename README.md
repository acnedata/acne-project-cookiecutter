# ACNE Project Cookiecutter

This is a [cookiecutter](https://cookiecutter.readthedocs.io/) template used to set up a fresh data project at ACNE
Data.

## Project structure
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
├── pyproject.toml        <- Here are all project dependencies listed. Some dev dependencies are already defined.
│
├── src                   <- Source code used in this project
│   └── __init__.py
└── tests                 <- Code for pytest.
    └── __init__.py
```

## Dependencies

To be able to properly work with this template some lodal dependencies need to be fullfilled. Namely `Git`, `DVC`, 
`cruft`, and `Poetry` need to be installed. If you are using the ACNE python dev container, all these will be in place.


## Usage

Move into the directory where you want to create a new project and run"
```bash
cruft create https://github.com/acnedata/acne-project-cookiecutter
```

You will be prompted to enter some information about this project such as the project name.

Initialize the 
