Software Quality Engineering — Unit Test Automation
Project Overview

This project focuses on unit test automation using Python and pytest as part of a Software Quality Engineering assignment.

The assignment extends the existing Python algorithms repository by adding automated unit tests for absolute-value-related functions, parameterized test cases, CSV-based data-driven testing, and pytest marker configuration.

Objectives
Implement automated unit tests for absolute-value-related functions.
Test positive, negative, zero, decimal, and list-based inputs.
Use pytest parameterization to test multiple input scenarios.
Implement data-driven testing using external CSV test data.
Configure custom pytest markers for test organization.
Maintain a spreadsheet of test cases for documentation.
Technologies Used
Python — programming language
pytest — unit testing framework
CSV — external test data
Git and GitHub — version control and repository hosting
Excel — test case documentation
Project Structure
SQE-Assignment-3/
├── tests/
│   └── test_abs_module.py
├── test_data/
│   └── abs_test_data.csv
├── docs/
│   └── Test_Cases.xlsx
├── pyproject.toml
└── README.md

Testing Scope

The automated tests cover the following functions imported from maths.abs:

abs_val()
abs_min()
abs_max()
abs_max_sort()

The test scenarios include:

Positive and negative numbers
Zero and decimal values
Lists containing positive and negative numbers
Single-element lists
Empty-list error handling
CSV-driven test cases for abs_val()
Data-Driven Testing

The file test_data/abs_test_data.csv contains input values and their expected results.

The CSV data is loaded and passed to pytest using parameterization, allowing the same test function to validate multiple input cases.

Pytest Configuration

The pyproject.toml file defines custom pytest markers used to categorize tests:

unit — identifies unit tests
csv_data — identifies tests that use external CSV data
How to Run the Tests
1. Clone the repository
git clone https://github.com/Hunaiza-ct/SQE-Assignment-3.git
cd SQE-Assignment-3

2. Create and activate a virtual environment

On Windows PowerShell:

python -m venv .venv
.\.venv\Scripts\Activate.ps1

3. Install pytest
python -m pip install pytest


Install any additional dependencies required by the project if necessary.

4. Run the assignment tests
python -m pytest tests/test_abs_module.py -v

5. Run CSV-driven tests only
python -m pytest tests/test_abs_module.py -m csv_data -v

6. Run unit tests only
python -m pytest tests/test_abs_module.py -m unit -v

Test Case Documentation

The Excel workbook docs/Test_Cases.xlsx is included to document the test cases associated with the assignment.

## Test Results

The assignment test suite was executed successfully.

- Total tests: 27
- Passed: 27
- Failed: 0
- Execution time: 0.34 seconds

Command used:

```powershell
python -m pytest tests/test_abs_module.py -v
Acknowledgements

This assignment builds upon the existing TheAlgorithms/Python open-source repository.

Credit for the original project and its existing source code belongs to its respective contributors. Assignment-specific test code, test data, configuration changes, and documentation are maintained as part of this coursework.

Author

Student Name: Hunaiza,sitara

Course: Software Quality Engineering

Project: Unit Test Automation Solution