# FEATURE ENGINEERING AND FEATURE SELECTION

## PROJECT OVERVIEW

This project demonstrates the application of feature engineering and feature selection techniques on the Titanic dataset. New features were created from existing data to improve predictive power, and multiple feature selection methods were used to identify the most informative predictors.

The project compares model performance before and after feature selection using Random Forest classification.

## OBJECTIVES

* Create meaningful features from existing variables
* Improve data representation through feature engineering
* Apply feature selection techniques to reduce dimensionality
* Compare model performance using different feature subsets
* Evaluate the impact of feature engineering on predictive accuracy
* Build a complete machine learning preprocessing workflow

## DATASET

### Titanic Dataset

The dataset contains passenger information from the Titanic disaster, including:

* Passenger Class
* Name
* Sex
* Age
* Fare
* Family Information
* Ticket Details
* Survival Status

### Target Variable

* Survived (0 = Did Not Survive, 1 = Survived)

## FEATURE ENGINEERING

Several new features were created to extract additional information from the dataset:

### Title

Passenger titles extracted from the Name column.

Examples:

* Mr
* Mrs
* Miss
* Master

### FamilySize

Calculated using:

FamilySize = SibSp + Parch + 1

### IsAlone

Binary feature indicating whether a passenger traveled alone.

### FarePerPerson

Calculated by dividing fare by family size.

### AgeBand

Passengers grouped into age categories.

## DATA PREPROCESSING

The workflow includes:

* Missing value imputation
* Categorical encoding
* Feature scaling
* ColumnTransformer construction
* Pipeline integration

## FEATURE SELECTION TECHNIQUES

### SelectKBest

Selects the most informative features using statistical tests and feature scoring.

### RFECV (Recursive Feature Elimination with Cross Validation)

Automatically identifies the optimal feature subset by repeatedly removing less important features and validating performance.

## MACHINE LEARNING MODEL

### Random Forest Classifier

Random Forest was used as the baseline model and for evaluating selected feature subsets.

## WORKFLOW

1. Load and explore the dataset
2. Engineer new features
3. Remove irrelevant variables
4. Split data into training and testing sets
5. Build preprocessing pipelines
6. Train a baseline Random Forest model
7. Apply SelectKBest feature selection
8. Train model using selected features
9. Apply RFECV feature selection
10. Train model using RFECV-selected features
11. Compare model performance

## KEY LEARNING OUTCOMES

* Feature Engineering
* Feature Selection
* SelectKBest
* RFECV
* Random Forest Classification
* Pipeline Construction
* ColumnTransformer
* Model Evaluation
* Feature Importance Analysis

## RESULTS

Feature engineering generated additional predictors that captured meaningful patterns in passenger data. Feature selection techniques helped identify the most informative variables while reducing feature complexity. Performance comparisons demonstrated the impact of engineered and selected features on model effectiveness.

## CONCLUSION

This project demonstrates how feature engineering and feature selection can improve machine learning workflows. By creating informative features and selecting the most relevant predictors, models can become more efficient, interpretable, and potentially more accurate.

