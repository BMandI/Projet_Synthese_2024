
# Preparation de l'environnement :

### 1) Création d’un repository central dans github :

- https://github.com/BMandI/Projet_Synthese_2024.git

### 2) Installation de cookiecutter-data-science pour la création de la structure du projet:

- Documentation sur : https://cookiecutter-data-science.drivendata.org/all-options/

```cmd
pip install cookiecutter-data-science
```

```cmd
ccds
```
![alt text](image.png)

![alt text](image-1.png)

On obtient la structure suivante :

## Project Organization

```
├── LICENSE            <- Open-source license if one is chosen
├── Makefile           <- Makefile with convenience commands like `make data` or `make train`
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── external       <- Data from third party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical data sets for modeling.
│   └── raw            <- The original, immutable data dump.
│
├── docs               <- A default mkdocs project; see mkdocs.org for details
│
├── models             <- Trained and serialized models, model predictions, or model summaries
│
├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
│                         the creator's initials, and a short `-` delimited description, e.g.
│                         `1.0-jqp-initial-data-exploration`.
│
├── pyproject.toml     <- Project configuration file with package metadata for src
│                         and configuration for tools like black
│
├── references         <- Data dictionaries, manuals, and all other explanatory materials.
│
├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
│
├── setup.cfg          <- Configuration file for flake8
│
└── src                <- Source code for use in this project.
    │
    ├── __init__.py    <- Makes src a Python module
    │
    ├── data           <- Scripts to download or generate data
    │   └── make_dataset.py
    │
    ├── features       <- Scripts to turn raw data into features for modeling
    │   └── build_features.py
    │
    ├── models         <- Scripts to train models and then use trained models to make
    │   │                 predictions
    │   ├── predict_model.py
    │   └── train_model.py
    │
    └── visualization  <- Scripts to create exploratory and results oriented visualizations
        └── visualize.py
```

--------
- Notre projet a été créé sur le Desktop :

![alt text](image-2.png)

### 3) Mettre a jour le Repository Github en versionnant notre code avec git en suivant les etapes suivantes :


```cmd
git init
```

```cmd
git add .
```

```cmd
git commit -m " Creation de la structure du projet"
```

```cmd
git remote add origin https://github.com/BMandI/Projet_Synthese_2024.git
```

```cmd
git branch -M main
```

```cmd
git push -u origin main
```
### 4) Installation de dvc et dvc-gdrive

lien de la documentation : https://dvc.org/doc

```cmd
pip install dvc
```

```cmd
pip install dvc-gdrive
```

### 5) Installation de MLFow :

lien de la documentation : https://www.mlflow.org/docs/2.3.1/quickstart.html

```cmd
pip install mlflow
```

### 6) Installation de Flask:

lien de la documentation : https://flask.palletsprojects.com/en/3.0.x/installation/

```cmd
pip install flask
```

### 7) Installation de Pytest:
lien de la documentation : https://docs.pytest.org/en/7.1.x/getting-started.html#install-pytest

```cmd
pip install -U pytest
```
### 8) Installation de feast:
lien de la documentation :https://docs.feast.dev/getting-started/quickstart

```cmd
pip install feast
```
### 9) Installation de evidently:
lien de la documentation :https://docs.evidentlyai.com/user-guide/install-evidently

```cmd
pip install evidently
```

### 10) Installation de Docker:
lien de la documentation :https://docs.docker.com/desktop/install/windows-install/

- On va mettre toutes les librairies a telecharger dans le fichiers requirements.txt et on execute la commande:

### 11) Creation d'un environement virtuel on l'appelle developpement:

```cmd
conda create --name developpement python=3.10 -y
```

```cmd
conda activate developpement
```

```cmd
pip install -r requirments.txt
```

### 12) Versionnement des données avec dvc:

- Initialiser dvc:

```cmd
dvc init
```

- Ajouter les données a traquer dans dvc:

```cmd
dvc add < path to data>
```

- Configurer Google Drive comme remote :

```cmd
dvc remote add -d myremote gdrive:// <path/to/remote>
```
Dans note cas  : path to remote = 1iRjRpzjmGq6Gd5Z0s1jNAJpJ_FP6hLT2

- Pousser les donner vers Google Drive:
```cmd
dvc push
```
