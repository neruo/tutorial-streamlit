# template for development with python3

The template repository for development with python3

## Directory

```shell
├── .vscode
│   ├── launch.json
│   └── settings.json
├── dataset
│   └── .gitkeep
├── python3-dev-template
│   ├── __init__.py
│   ├── argument.py
│   └── run.py
├── tests
│   └── .gitkeep
├── .gitignore
├── LICENSE
├── README.md
├── poetry.lock
└── pyproject.toml
```

## Prerequisites

- Installed [Poetry](https://github.com/python-poetry/poetry) (>=1.1.8), [Git](https://git-scm.com/) (>=2.17.1)

## Create repository command memo

```shell
# git clone this repository
git clone https://github.com/neruo/python3-dev-template.git
cd ~/workspace/python3-dev-template

# setup poetry
poetry init -n
poetry env use python # create virtual environment
poetry add --dev poethepoet flake8 black isort mypy jupyterlab pytest mlflow
poetry shell # attach virtual environment

# setup vscode files: launch.json settings.json
git clone https://gist.github.com/278955c697d3788500e77521e57c47bb.git .vscode
rm -r .vscode/.git

# create start files: __init__.py run.py argument.py
git clone https://gist.github.com/c7830fa9d7aa62581b91da6d4a028ae3.git python3-dev-template
rm -r python3-dev-template/.git
```

## Development usage

```shell
# setup poetry
poetry install # install packages
poetry shell # attach virtual environment
poe mkl # add numpy scipy with IntelMKL
poe torch-cu111# #add torch+cu111, torchvision+cu111
```
