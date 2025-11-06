# Access to TONe Integrated Cloud Observatory data repos

This repo contains a [tutorial notebook](tutorial_tone_ico_data_access.ipynb) and the definition of a Python virtual environment (.python-verions, pyproject.toml, uv.lock) for accessing data repos from the Troll Observing Network's Integrated Cloud Observatory.

## STEP 1) Create a reproducible Python virtual environment

### Install [the uv package manager](https://docs.astral.sh/uv/getting-started/installation/)

The command below can be executed from anywhere on your local computer (laptop, desktop, workstation, ...), because the shell script will install the executable in the appropriate place and put the location on your path.

```{bash}
# For Linux and Mac
curl -LsSf https://astral.sh/uv/install.sh | sh

# Test the installation; you should see a list of available uv commands
uv 
```

### Build the Python virtual environment

The commands below need to be executed from the base directory of the repo; /integrated-cloud-observatory-team

```{bash}
# Deactivate any current virtual environments
deactivate

# Build .venv using uv
uv sync
```

### Use the virtual environment in IPython or Jupyter Lab

The commands below start either an IPython shell or Jupyter Lab with the installed Python virtual environment

- IPython

```{bash}
uv run ipython
```

- Jupyter Lab

```{bash}
uv run jupyter-lab
```

### Set the Python Interpreter in VSCode

If you're using VSCode, open the Command Pallette (e.g., command-shift-P on a Mac), then type ```Python: Select Interpreter```. Choose ```.venv/bin/python``` to select the virtual environment associate with this code repository.

## STEP 2) Start the tutorial

- Open the [tutorial notebook](tutorial_tone_ico_data_access.ipynb) in either VSCode or JupyterLab to access the data repos!
