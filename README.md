
# ToxiGuard: Marine Biotoxin Risk Prediction

## Overview

ToxiGuard is a machine learning project designed to analyse marine biotoxin data and estimate toxin risk using available environmental and sampling information.

The project uses two machine learning approaches:
1. Random Forest Classifier for risk classification.
2. Random Forest Regressor for toxin concentration prediction.

This project is developed for academic and research purposes.

## Objectives

- Analyse marine biotoxin measurements.
- Integrate toxin data with available hydrographic and phytoplankton information.
- Perform data cleaning and exploratory data analysis.
- Classify samples into data-defined High Risk and Low Risk categories.
- Estimate toxin concentrations for supported toxin groups.
- Evaluate model performance using appropriate metrics.
- Provide an interactive interface for sample predictions.

## Machine Learning Models

### 1. Random Forest Classifier

The classifier predicts whether a sample belongs to the High Risk or Low Risk category.

Evaluation metrics:
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- PR-AUC
- Confusion Matrix

### 2. Random Forest Regressor

The regressor predicts numerical toxin concentrations for toxin groups with sufficient usable measurements.

Evaluation metrics:
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R-squared (R²)

The classifier predicts a category, whereas the regressor predicts a numerical concentration.

## Dataset

The project uses three categories of data:

- Marine biotoxin measurements
- Hydrographic and environmental observations
- Toxic phytoplankton observations

The datasets are cleaned and integrated using compatible station and date information.

Some measurements may be reported as below or above a detection or reporting limit. These records must be interpreted carefully during preprocessing.

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Joblib
- OpenPyXL

## Project Workflow

1. Load the datasets.
2. Clean and preprocess the data.
3. Integrate available environmental observations.
4. Perform exploratory data analysis.
5. Prepare features and target labels.
6. Split observations chronologically into training, validation and test sets.
7. Train the Random Forest Classifier.
8. Evaluate classification performance.
9. Train Random Forest Regression models for supported toxin groups.
10. Evaluate concentration predictions.
11. Save model artifacts and evaluation results.
12. Generate predictions through the interactive interface.

## How to Run

1. Open the notebook in Google Colab.
2. Upload the required datasets.
3. Verify dataset filenames and file paths.
4. Execute the notebook cells in order.
5. Review the preprocessing summaries and EDA plots.
6. Train and evaluate the machine learning models.
7. Inspect the classification and regression results.
8. Run the prediction interface if required.
9. Download the generated results if the saving cells complete successfully.

## Evaluation

Classification performance is assessed using accuracy, precision, recall, F1-score and other classification metrics.

Regression performance is assessed using MAE, RMSE and R².

The final test-set results should be used when reporting model performance. Actual metric values must be taken from a successful notebook execution rather than assumed or manually estimated.

## Limitations

- Model performance depends on dataset quality and coverage.
- Missing environmental measurements may affect predictions.
- Censored measurements can reduce the number of usable training records.
- Some toxin groups may have insufficient exact measurements for reliable regression.
- Data-derived risk labels are not official regulatory safety thresholds.
- Performance on historical observations does not guarantee future accuracy.

## Future Enhancements

- Incorporate additional verified environmental observations.
- Improve the handling of censored toxin measurements.
- Evaluate additional machine learning algorithms.
- Improve performance on underrepresented high-risk samples.
- Validate predictions on independent datasets.
- Enhance the interactive dashboard and reporting system.

## Disclaimer

ToxiGuard is an academic machine learning prototype. Its predictions are estimates and must not be treated as official food-safety certifications or substitutes for laboratory testing and applicable regulatory guidance.
