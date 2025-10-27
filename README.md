# Prices Predictor System

## Overview

This project is an end-to-end machine learning system for predicting house prices using the Ames Housing dataset. Leveraging modern ML best practices, it includes automated data ingestion, preprocessing, feature engineering, model building, evaluation, and deployment pipeline.

## Setup Instructions

1. **Clone this repository**
2. **Install Python dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
3. **Configure the project** (if needed):
   - Edit `config.yaml` to set paths or parameters as required.

## How to Run

### Train a Model

```bash
python run_pipeline.py
```

This executes the end-to-end ML pipeline: ingestion, splitting, preprocessing, feature engineering, model training, and evaluation. Artifacts and metrics are tracked via MLflow (`mlruns/`).

### Deploy the Model Pipeline

```bash
python run_deployment.py
```

This loads the trained model and provides deployment/inference-ready utilities.

### Sample Prediction

```bash
python sample_predict.py
```

Reference how to use the trained model to make individual predictions.

## Workflow & Pipeline

- **Data Ingestion** (`steps/data_ingestion_step.py`)
- **Train-test Split** (`steps/data_splitter_step.py`)
- **Missing Value Handling** (`steps/handle_missing_values_step.py`)
- **Feature Engineering** (`steps/feature_engineering_step.py`)
- **Outlier Detection** (`steps/outlier_detection_step.py`)
- **Model Building** (`steps/model_building_step.py`)
- **Evaluation** (`steps/model_evaluator_step.py`)
- **Deployment Utils** (`steps/model_loader.py`, `steps/prediction_service_loader.py`)

## EDA & Analysis

See `analysis/EDA.ipynb` and scripts in `analysis/analyze_src/` for insights and exploratory data analysis.

## MLflow Tracking

All experimental runs and metrics are tracked in the `mlruns/` directory using [MLflow](https://mlflow.org/).

## Contributing

Contributions, issues, and feature requests are welcome! Please fork the repository and submit a pull request, or open an issue for larger proposals.

