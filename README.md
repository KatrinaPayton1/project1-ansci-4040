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

This project will take place over 4 weeks, with the following timeline:

### Week 1 (9/15-9/22): Setup and understand data
- Create public repository
- Set up the notebook  for inspection
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
The best model depends on the target variable and the structure of the dataset. I plan to start with a  baseline **logistic regression** for classification . This model works well for tabular data,  mixed variable types, and nonlinear relatinships.
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

