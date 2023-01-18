# ACNE Data Project Template

This is a template to guide set up of a fresh data project at ACNE Data.

## Folder structure
```
client-YYYY(-project)    <- The top-level repository in the stated naming convention.
│                           (e.g. acne-2022). Optionally with a project description (e.g. acne-2022-workplace-survey)
│
├── .devcontainer/       <- Configuration files for GitHub Codespaces.
│
├── .github/             <- Configuration files for GitHub Actions.
│   └── workflows/
│
├── .gitignore           <- Files and directories that git should ignore.
│
├── .pre-commit.yaml     <- Configuration file for pre-commit.
│
├── README.md            <- The top-level README with a brief description of this project.
│
├── data/                <- Here data used in the project can be stored. These should only be small (< 1MB) files
│                           as github has a restriction on repository size (100 MB).
│
├── notebooks            <- Jupyter notebooks used for data exploration and code experimentation.
│                           Naming convention is initials-number-description. The number is for
│                           ordering purposes and is incremented with every new notebook.
│                           (e.g. iw-1-data-exploration)
│
├── pyproject.toml       <- Here are all project dependencies listed.
├── poetry.lock          <- This is where Poetry describes how to replicate the environment.
│
├── src                  <- Source code used in this project.
│   └── __init__.py
│
└── tests                <- Code for pytest, if applicable.
    └── __init__.py
```

## Initialization
1. Setup a new repository on GitHub.
2. Clone that repo on your local machine or start a Codespaces instance.
3. Follow the instructions on [repo-config](https://github.com/acnedata/repo-config) to get some 
basic configuration files.
4. If you are on Codespaces, rebuild your container to get dependencies in place.

## Dependency managment with Poetry

We manage our depencies with [Poetry](https://python-poetry.org/).

To get started we only need four basic commands `init`, `add`, `run`, and `install`.

1. We create a new `pyproject.toml` file by running:
```
poetry init
```

If you are planning to put all code into a `src` directory, make sure to add
```toml
packages = [{include = "src"}]
```
add the end of the `[tool.poetry]` block.

2. To add a library like Pandas to our Python environment, we just have to run
```
poetry add pandas
```

This creates a `poetry.lock` file that we have to make sure to version control as well.
Check out the [documentation](https://python-poetry.org/docs/dependency-specification/) to learn 
how dependency constraints are specified in Poetry.

3. To execute a script we have to run
```
poetry run python src/myscript.py
```

4. If we are joining an already set up project that has a `poetry.lock` file, we can install all
specifed dependencies by running
```
poetry install
```

To learn more about how to use this tool
check their [documentation](https://python-poetry.org/docs/basic-usage/).

## Linting with pre-commit

To guarantee a consistent code style and help us stick to best practices, we are using a few
autoformatters and linters. If you followed the steps from 'Initilization' and are working in
GitHub Codespaces, everything is set up already for you!

To check if your code is up to standard before pushing your commits, all you have to do is run
```
pre-commit run --all
```

## Documentation

- [Git](https://git-scm.com/doc)
- [GitHub CLI](https://cli.github.com/manual/index)
- [GitHub Codespaces](https://docs.github.com/en/codespaces/overview)
- [Poetry](https://python-poetry.org/docs/)
- [pre-commit](https://pre-commit.com/index.html)
