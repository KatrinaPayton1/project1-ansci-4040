# project1-ansci-4040

This repository is a workspace for Project 1 of ANSC 4040.

## Project Overview

The goal of this project is to work with the project dataset that is currently missing table values with an end goal of matching each cow to their statistics and predicting the remaining values. To do so, I must use skills that I have learned thus far in this course to, clean and inspect the data, build a reproducible modeling workflow, and summarize the findings in a clear and defensible way. 

## Working Environment (Local vs. Cloud)
- Primary approach: local environment, commiting changes to the cloud
- IDE: VS Code
- Language: Python
- Tools: Jupyter notebooks, pandas, Git

## Timeline

This project will take place over 4 weeks, with the following timeline:

### Week 1 (9/15-9/22): Setup data
- Create public repository
- Set up the notebook for inspection
- Confirm the dataset structure and file format


### Week 2 (9/22-9/29): Data understanding, cleaning and preparation
- Run an initial exploratory data analysis (make a data profile report)

*Cleaning Data*
- Identify and remove data duplicates 
- Perform a Z score inspection to determine and remove outliers based on a standard deviation of 3
- Assess remaining zero values: 
    1. Determine where zero values are present 
    2. Compare zero and non-zeero values withing remaining rows, keep only those in which zero values are present for Flow30_60Session. These values are plausibly missing and will need to be filled later. 
- Assess remaining missing values: 
    1. Identify rows in which non-outcome values missing
    2. Decide to either remove or fill the values in these rows through taking averages etc. (I removed them due to small percentage)

*Prepare training, testing and validation data splits*
- After cleaning, the data set was reduced from about 8.4 million rows to 6.6 million.
- The planned split is as follows
    70% Train data
    20% Internal validation data  ------- External Validation will be excluded from this set
    10% Test
- Important considerations for this split: To prevent data leakage, it is best to split by time, removing future dates from trianing. This will prevent the model from using known dates to assist with its prediction. 
- Plan for the split: 
    1. Sort by date and cow, and split ensuring each cow in test set represented in training set
    2. Keep the most recent dates in the test set (10%)
    3. Use earlier dates for training (70%)
    4. Use a validation window between them (20%)


### Week 3 (9-29-10/06): Baseline modeling, refining, and validation
- Train a RandomForestClassification tree-based model
- Check validation set performance: accuracy, classification metrics
- Optimize hyperparameters with a grid search to improve accuracy and prevent overfitting 
    *N_estimators*(numbers of trees... more to be stable)
    *max_depth* (depth of tree growth... closer data fitting)
    *min_samples_split* (min samples to split internal node... higher values are conservative)
    *min_samples_leaf* (min samples that must be in leaf node... higher values for less complexity)
- Use test data set with model and assess accuracy
confirm that the model output is reasonable and not just overfit to noise

### Week 4: Final Presentation
- Prepare the final results, charts, and interpretation
- Summarize the methods and conclusions in a clear poster 

### Model choice
The best model depends on the target variable and the structure of the dataset. I plan to start with a **RandomForestClassification** tree-based model, which takes predictions of multiple individual decision trees through bagging and feature randomness, and combines them to fill in the target variable, which I define as AnimalId.

IMPORTANT NOTE: This model does not work for predicting new cows not identifiable in the training set, and thus this model would not be transferable to a new farm.  

### Testing approach
I will include the following checks throughout the project:
- verify the dataset schema and variable types
- check missing values before and after cleaning
- use a train/validation/test split or cross-validation
- compare performance with clear evaluation metrics
- confirm that the model output is reasonable and not just overfit to noise

### Data lineage/Reproducibility
I plan to keep the project reproducible, by tracking the flow of the data from raw file to final modeled output:
- keep the original dataset in the repo or a clearly labeled raw-data folder
- document any cleaning decisions in notebooks
- save processed versions with meaningful names
- Make commits as I edit and version controlled with Git
- use markdown cells to label assumptions and explanations 