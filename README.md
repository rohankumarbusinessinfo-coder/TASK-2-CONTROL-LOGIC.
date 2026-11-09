Task 2: Control Logic – Data Cleaning Automation

1. Project Overview

This project defines the control logic for an automated data cleaning and reporting system using Python and Pandas.

The system processes datasets, identifies errors, cleans data, validates results, and generates reports.

2. System States

The automation system consists of the following states:

1. START: Initialize the automation process.
2. INPUT: Accept CSV or Excel datasets.
3. VALIDATION: Check file format, column names, and data availability.
4. DATA CLEANING: Handle missing values, remove duplicates, and standardize formats.
5. QUALITY CHECK: Verify the cleaned dataset.
6. REPORT GENERATION: Generate summary reports.
7. COMPLETED: Save the final output.
8. ERROR / STOP: Stop processing if a critical error occurs.

3. Inputs

- CSV or Excel dataset.
- File location and name.
- Required column information.
- Missing-value handling rules.
- Duplicate detection rules.
- Data validation requirements.

4. Outputs

- Cleaned dataset.
- Summary of missing values.
- Duplicate records report.
- Data quality validation results.
- Final Excel or CSV report.
- Error messages when processing fails.

5. Safety Stops

The system must stop processing under these conditions:

- Input file is missing or inaccessible.
- File format is unsupported.
- Required columns are missing.
- Dataset is empty or corrupted.
- Data validation fails.
- Output file cannot be saved.

The original dataset must never be overwritten. A separate output file should be created to prevent accidental data loss.

6. Pseudocode

BEGIN

Initialize automation system

IF input file does not exist:
    STOP and display error

Load CSV or Excel dataset

IF dataset is empty:
    STOP and display error

Check required columns

IF required columns are missing:
    STOP and display error

Identify missing values
Identify duplicate records

Clean missing values according to defined rules
Remove duplicate records
Standardize data formats

Validate cleaned dataset

IF validation fails:
    STOP and display error

Generate summary report

Save cleaned data in a new output file

IF output file is saved successfully:
    Display "Process Completed Successfully"
ELSE:
    STOP and display save error

END

7. Expected Result

The control logic ensures that the data cleaning process follows a structured sequence, produces reliable outputs, and stops safely whenever critical errors occur.

Project Status: Control logic documented. Program implementation and testing are pending.