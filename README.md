# Hospital_readmission_data_analysis
Predicting hospital readmission for diabetic patients using machine learning and EDA. This repository contains code for data preprocessing, model training and evaluation to identify patients at high risk of readmission within 30 days. Also some other insightful excel and word doc for good interpretation.
# Hospital Readmission Prediction for Diabetic Patients

[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python Version](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![Libraries](https://img.shields.io/badge/Libraries-Pandas%2C%20NumPy%2C%20Scikit--learn%2C%20XGBoost-brightgreen.svg)](https://pypi.org/)
[![Contributions Welcome](https://img.shields.io/badge/Contributions-Welcome-orange.svg)](https://github.com/your-username/your-repo-name/blob/main/CONTRIBUTING.md) ## Overview

This project aims to predict the likelihood of hospital readmission within 30 days for diabetic patients using machine learning techniques. By analyzing a dataset of patient records, we develop and evaluate classification models to identify individuals at high risk of early readmission. This information can be valuable for healthcare providers to implement targeted interventions and improve patient care, potentially reducing readmission rates and associated costs.

The project encompasses data preprocessing, exploratory data analysis (EDA), model training (with a focus on Random Forest and XGBoost), and comprehensive model evaluation.

## Table of Contents

- [Overview](#overview)
- [Table of Contents](#table-of-contents)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Data](#data)
  - [Data Source](#data-source)
  - [Data Description](#data-description)
- [Project Structure](#project-structure)
- [Methodology](#methodology)
  - [Data Preprocessing](#data-preprocessing)
  - [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
  - [Model Training](#model-training)
  - [Model Evaluation](#model-evaluation)
- [Results](#results)
  - [Random Forest](#random-forest)
  - [XGBoost](#xgboost)
  - [Comparison](#comparison)
- [Potential Improvements](#potential-improvements)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Getting Started

### Prerequisites

Before running the code, ensure you have the following installed:

- **Python 3.x** (recommended) - You can download it from [https://www.python.org/downloads/](https://www.python.org/downloads/)
- **pip** (Python package installer) - Usually included with Python installations.

### Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    cd your-repo-name
    ```
    (Replace `https://github.com/your-username/your-repo-name.git` with the actual URL of your repository.)

2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    # On Windows:
    # venv\Scripts\activate
    # On macOS and Linux:
    source venv/bin/activate
    ```

3.  **Install the required libraries:**
    ```bash
    pip install -r requirements.txt
    ```
    (You'll need to create a `requirements.txt` file listing all the dependencies. A basic one would look like this):
    ```
    pandas
    numpy
    matplotlib
    seaborn
    scikit-learn
    xgboost
    scipy
    imblearn
    ```

## Data

### Data Source

The dataset used in this project contains records of diabetic patients and their hospital encounters. [If the data is publicly available, provide a link and citation here. If not, describe the nature of the data generally, e.g., "The data was obtained from a hospital database and includes features such as demographic information, medical history, diagnoses, medications, and hospital stay details."]

### Data Description

The dataset includes various features related to patient demographics, medical conditions, medications, and hospital visits. Key features include:

- [List a few important features and briefly describe them. For example:]
    - `race`: Patient's race.
    - `gender`: Patient's gender.
    - `age`: Patient's age group.
    - `admission_type_id`: Type of hospital admission.
    - `discharge_disposition_id`: Status of patient at discharge.
    - `diag_1`, `diag_2`, `diag_3`: Primary, secondary, and tertiary diagnoses.
    - `medications`: Information about prescribed medications.
    - `A1Cresult`: Result of A1C test.
    - `max_glu_serum`: Maximum glucose serum test result.
    - `readmitted`: The target variable indicating if the patient was readmitted within 30 days (`<30`), after 30 days (`>30`), or not readmitted (`NO`). This was transformed into a binary target (1 for `<30`, 0 for `>30` or `NO`).

## Project Structure
