# project1-ansci-4040

This repository is a workspace for Project 1 of ANSC 4040.

## Project Overview

The goal of this project is to work with the project dataset that is currently missing table values with an end goal of matching each cow to their statistics and predicting the remaining values. To do so, I must use skills that I have learned thus far in this course to, clean and inspect the data, build a reproducible modeling workflow, and summarize the findings in a clear and defensible way. 
## Working Environment (Local vs. Cloud)
- Primary approach: local development, commiting changes to the cloud
- IDE: VS Code
- Language: Python
- Tools: Jupyter notebooks, pandas, Git


## Timeline

This project will take place over approximately 4 weeks, with the following timeline:

### Week 1 (9/15-9/22): Setup and understand data
- Create public repository
- Set up the notebook workflow for inspection
- Confirm the dataset structure and file format
- Run an initial exploratory data analysis
- Identify data quality problems, missing values, and schema issues


### Week 2 (9/22-9/29): Data cleaning and preparation
- Handle missing values and inconsistent entries
- Check data types and verify target variables
- Create a clean dataset for modeling
- Prepare training and validation data splits

### Week 3 (9-29-10/06): Baseline modeling, refining, and validation
- Train a simple baseline model
- Use model for my data

- Run validation checks and cross-validation where appropriate
- Review error patterns and stability of the model

### Week 4: Final Presentation
- Prepare the final results, charts, and interpretation
- Summarize the methods and conclusions in a clear poster 
## Strategy and Brainstorm

### Model choice
The best model depends on the target variable and the structure of the dataset. I plan to start with a simple, interpretable baseline such as logistic regression for classification or linear regression for continuous outcomes, depending on the project goal. If that is not sufficient, I will compare it against a stronger model such as a random forest or gradient boosting method.

The key principle is to begin with a simple and interpretable model before moving to more complex methods. This keeps the workflow easier to explain and makes it easier to diagnose problems.

### Testing approach
I will include the following checks throughout the project:
- verify the dataset schema and variable types
- check missing values before and after cleaning
- use a train/validation/test split or cross-validation
- compare performance with clear evaluation metrics
- confirm that the model output is reasonable and not just overfit to noise

### Data lineage
To keep the project reproducible, I will track the flow of the data from raw file to final modeled output:
- keep the original dataset in the repo or a clearly labeled raw-data folder
- document any cleaning decisions in notebooks or scripts
- save processed versions with meaningful names
- track major transformations and keep the workflow version controlled with Git

This is important because it makes it easier to explain how results were produced and debug any issues if the analysis changes over time.

### Reproducibility and documentation
- Keep notebooks organized by stage: inspection, cleaning, modeling, evaluation
- Use clear markdown notes to explain model choices and assumptions
- Save key plots and summary tables for later review
- Keep code version-controlled so results can be regenerated

## Wednesday Discussion Preparation

Before Wednesday, I will prepare the following:
- a quick summary of the dataset and variables
- the list of candidate modeling approaches
- a description of data quality issues or assumptions
- a plan for testing and validation
- a clear decision on whether a local or cloud workflow is more appropriate
