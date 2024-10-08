# adv_mla_at2_exp

<a target="_blank" href="https://cookiecutter-data-science.drivendata.org/">
    <img src="https://img.shields.io/badge/CCDS-Project%20template-328F97?logo=cookiecutter" />
</a>

This project focuses on building two models for an American retailer with 10 stores across California, Texas, and Wisconsin. The first model is a machine learning-based predictive model to estimate daily sales revenue for specific items at individual stores. The second model is a time-series forecasting model that predicts total sales revenue across all stores and items for the next 7 days. The models are deployed as APIs using Streamlit to provide real-time predictions and forecasts for business use.

## Project Organization

```
├── LICENSE                <- Open-source license if one is chosen.
├── Makefile               <- Makefile with convenience commands like `make data` or `make train`.
├── README.md              <- The top-level README for developers using this project.
├── data
│   ├── external           <- Data from third party sources.
│   ├── interim            <- Intermediate data that has been transformed.
│   ├── processed          <- The final, canonical data sets for modeling.
│   └── raw                <- The original, immutable data dump.
│
├── docs                   <- A default mkdocs project; see www.mkdocs.org for details.
│   └── .gitkeep           <- Placeholder to keep the docs directory in version control.
│   └── mkdocs.yml         <- Configuration file for MkDocs documentation.
│
├── models                 <- Trained and serialized models, model predictions, or model summaries.
│   ├── forecasting        <- Folder for forecasting models.
│   ├── predictive         <- Folder for predictive models.
│   └── .gitkeep           <- Placeholder to keep the models directory in version control.
│
├── notebooks              <- Jupyter notebooks.ipynb files are stored here.                       
│   ├── forecasting        <- Folder for forecasting notebooks.
│   ├── predictive         <- Folder for predictive notebooks.
│   └── .gitkeep           <- Placeholder to keep the notebooks directory in version control.
│
├── pyproject.toml         <- Project configuration file with package metadata for adv_mla_at2_exp
│                             and configuration for tools like black.
│
├── references             <- Data dictionaries, manuals, and all other explanatory materials.
│
├── reports                <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures            <- Generated graphics and figures to be used in reporting.
│
├── requirements.txt       <- The requirements file for reproducing the analysis environment, e.g.
│                             generated with `pip freeze > requirements.txt`.
│
├── setup.cfg              <- Configuration file for flake8.
│
└── adv_mla_at2_exp        <- Source code for use in this project.
    ├── __init__.py        <- Makes adv_mla_at2_exp a Python module.
    ├── config.py          <- Stores useful variables and configuration.
    ├── dataset.py         <- Scripts to download or generate data.
    ├── features.py        <- Code to create features for modeling.
    ├── modeling           <- Directory containing model-related code.
    │   ├── __init__.py    <- Marks the modeling directory as a Python package.
    │   ├── predict.py     <- Code to run model inference with trained models.
    │   └── train.py       <- Code to train models.
    └── plots.py           <- Code to create visualizations.
```

--------

# Project Instructions

All the code files are located in the `notebooks` section. Within this section, there are two folders:
- **predictive**: Contains notebooks related to predictive modeling.
- **forecasting**: Contains notebooks related to forecasting models.

## Step-by-Step Setup

1. **Install Requirements**:
   - Before running the models, install the necessary dependencies by running the `requirements.txt` file on your local computer:
     ```bash
     pip install -r requirements.txt
     ```

2. **Download Data Files**:
   - Access the data files from [this Google Drive link](https://drive.google.com/drive/folders/1rlqh5eOR-eImzU6DAqt3RDl3VZ9AkaGv?usp=share_link).
     - If you want to load all data files from the beginning, navigate to the `raw` folder and download all 5 CSV files.
     - If you prefer to use the merged dataset, go to the `processed` folder and download `df_train_long` and `df_train_test`.
     - If you only want to train the model, download `df_train_reduced`, `df_validation_reduced`, and `df_test_reduced` from the `processed` folder.

## Running the Streamlit App

1. **Install Requirements for the Main App**:
Before running the Streamlit app, make sure to install the necessary dependencies for the main application:

```bash
pip install -r requirements.txt
```
2. **Clone the Repository**:
   - Clone the entire repository. The link to the GitHub repository is provided in the `github.txt` file.

3. **Download Model Artifacts**:
   - You can either clone the whole repository or simply download the necessary artifacts from the `models` folder to run the app.

4. **Run the App**:
   - Download the `main.py` file from the API repository, as shared in `github.txt`.
   - After setting up everything , open your terminal and run:

     ```bash
     streamlit run app/main.py
     ```
   - This will launch the Streamlit app. Make sure you have installed the dependencies from `requirements.txt` before starting the app.

## Additional Notes

- Ensure you follow the directory paths as specified above to avoid any file loading issues.
- If you encounter any issues, verify that all required files are in the correct locations and that the environment is set up as per the instructions.