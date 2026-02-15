# Student Dropout Prediction

A machine learning project to predict student dropout risk using historical academic and engagement data.

## Overview

This project analyzes student behavior and academic performance to identify at-risk students early. It uses data from the Open University Learning Analytics (OULA) dataset to build predictive models that can help educational institutions intervene before students drop out.

## Contents

- [Project Structure](#project-structure)
- [Data](#data)
- [Models](#models)
- [Getting Started](#getting-started)
- [Results](#results)

## Project Structure

```
oula_analysis/
├── student-dropout-prediction.ipynb        # Main analysis and modeling notebook
├── data/                                   # Dataset files
│   ├── assessments.csv                     # Assessment details and scores
│   ├── studentAssessment.csv               # Individual student assessment results
│   ├── studentInfo.csv                     # Student demographic and enrollment info
│   ├── studentRegistration.csv             # Student registration records
│   ├── studentVle.csv                      # Student virtual learning environment interactions
│   ├── courses.csv                         # Course information
│   ├── vle.csv                             # Virtual learning environment resources
│   ├── BBB_2013B_day30_preprocessed.csv    # Preprocessed data for 2013B cohort (day 30)
│   └── BBB_2014B_day30_preprocessed.csv    # Preprocessed data for 2014B cohort (day 30)
└── models/                                 # Trained model files
    ├── best_model_BBB_2013B_day30.joblib   # Optimized model for 2013B
    └── scaler_BBB_2013B_day30.joblib       # Feature scaler for 2013B
```

## Data

The project utilizes the Open University Learning Analytics (OULA) dataset, which includes:

- **Student Demographics**: Demographic information and enrollment status
- **Assessment Data**: Course assessments and student performance
- **Learning Interactions**: Virtual Learning Environment (VLE) activity logs
- **Registration Records**: Course registration and module information

### Dataset Download

The datasets are not included in this repository due to size constraints. Download the data from the Open University Learning Analytics portal:

https://analyse.kmi.open.ac.uk/open-dataset

### Data Files

- `assessments.csv`: Assessment item information
- `courses.csv`: Course catalog
- `vle.csv`: Virtual Learning Environment resources
- `studentInfo.csv`: Student attributes and outcomes
- `studentAssessment.csv`: Student performance on assessments
- `studentVle.csv`: Student interactions with VLE materials
- `studentRegistration.csv`: Student course registrations
- `BBB_2013B_day30_preprocessed.csv`: Processed features at 30-day mark (2013B)
- `BBB_2014B_day30_preprocessed.csv`: Processed features at 30-day mark (2014B)

## Models

The project includes trained models optimized for early prediction (at 30 days into the course):

- `best_model_BBB_2013B_day30.joblib`: Best performing classifier for 2013B cohort
- `scaler_BBB_2013B_day30.joblib`: Feature scaling transformer for normalization

## Getting Started

### Prerequisites

- Python 3.7+
- Jupyter Notebook
- Required packages: pandas, numpy, scikit-learn, joblib

### Installation

1. Clone or download the project
2. Download the datasets:
   - Visit https://analyse.kmi.open.ac.uk/open-dataset
   - Download the required OULA datasets
   - Extract the CSV files into the `data/` directory
3. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn joblib jupyter
   ```

### Usage

1. Open the Jupyter notebook:
   ```bash
   jupyter notebook student-dropout-prediction.ipynb
   ```

2. Run the cells to:
   - Load and explore the data
   - Preprocess and engineer features
   - Train and evaluate prediction models
   - Make predictions on new data

## Results

The models are trained to predict student dropout risk early in the academic term, enabling timely interventions. Models are evaluated on their ability to identify at-risk students with high accuracy.