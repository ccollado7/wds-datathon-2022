WiDS Datathon 2022
==============================

Repository for the competence Women in Data Science (WiDS) 2022 https://www.kaggle.com/c/widsdatathon2022/overview/description

Model Tacking https://docs.google.com/spreadsheets/d/14KdfXp5V8n0fMZVpESDIf3DokJbbEwGSJ93EKtUtRMs/edit#gid=0

## Pre-Requirements

* [git](https://git-scm.com/downloads)
* [anaconda](https://www.anaconda.com/products/individual) / [minconda](https://docs.conda.io/en/latest/miniconda.html)

### Steps

**Step 1**: Download the repository.

```bash
$ git clone https://github.com/ccollado7/wds-datathon-2022.git
$ cd wds-datathon-2022
```

**Step 2**: Create environment dependencies for the project (Stopped in the project directory).

```bash
$ conda env create -f environment.yml
```

**Step 3**: Activate the environment where the project dependencies are installed.

```bash
$ conda activate wds-datathon-2022
```

**Paso 4**: On the project directory we raise jupyter lab or jupyter notebook

```bash
$ jupyter lab

Jupyter Notebook 6.1.4 is running at:
http://localhost:8888/?token=45efe99607fa6......
```

**Step 5**: Go to http://localhost:8888.... as indicated in the console.

## Add a new dependency

**Step 1**: Add the new dependency to ´environment.yml´

Conda has its own package repositories but in case of any problems you can always use the pip packages.

```yaml
...
dependencies:
  - CONDA_PACKAGE
  - CONDA_PACKAGE
  - pip:
    - PIP_PACKAGE
    - PIP_PACKAGE
...
```

**Step 2**: Once we add the name of the new package in ´environment.yml´ it remains to install it. For this we must **update** our environment with the changes we made in ´environment.yml´ as follows:

```bash
$ conda env update -f environment.yml
```
**Step 3**: Finally, if we had **jupyter lab** open, we must restart the kernel where our notebook is running in order to load the new library.

![image](https://user-images.githubusercontent.com/962480/145253730-365cb56b-ae26-41b0-a38d-41d505c9ea74.png)



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

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
