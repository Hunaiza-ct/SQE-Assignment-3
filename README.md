## SQE Assignment: Unit Testing and Test Automation

### Project Overview

This assignment uses the open-source **TheAlgorithms/Python** project to demonstrate automated unit testing with Python and pytest.

The selected test module is `maths.abs`. The tests cover absolute value calculation, minimum and maximum values, sorting-based maximum calculation, empty-list error handling, and CSV-based data-driven testing.

### Development Environment

- Operating System: Windows
- Python: 3.15.0
- pytest: 9.1.1
- pytest-xdist: 3.8.0
- Test Framework: pytest

### Project Files

- `tests/test_abs_module.py` — automated unit tests
- `test_data/abs_test_data.csv` — external CSV test data
- `docs/Test_Cases.xlsx` — Excel test cases and execution summary
- `pyproject.toml` — pytest configuration and test markers

### Test Design Techniques

The tests use the following techniques where applicable:

- **Equivalence Class Partitioning (ECP):** testing positive, negative, zero, and empty-list inputs.
- **Boundary Value Analysis (BVA):** checking values around zero and other representative numeric inputs.
- **Parameterized Testing:** running the same test function with multiple input and expected-output combinations.
- **Data-Driven Testing:** loading test inputs and expected results from a CSV file.
- **Exception Testing:** checking the expected `ValueError` for empty-list inputs.

### Setup Instructions

1. Install Python and ensure it is available in PATH.
2. Open PowerShell in the project directory.
3. Create a virtual environment:

   ```powershell
   python -m venv .venv
   ```

4. Activate the virtual environment:

   ```powershell
   .\.venv\Scripts\Activate.ps1
   ```

5. Install the required testing packages:

   ```powershell
   python -m pip install pytest pytest-xdist
   ```

### Running the Tests

Run the complete test suite:

```powershell
python -m pytest tests/test_abs_module.py -v
```

Run CSV-based tests only:

```powershell
python -m pytest tests/test_abs_module.py -m csv_data -v
```

Run tests marked as unit tests:

```powershell
python -m pytest tests/test_abs_module.py -m unit -v
```

Run tests in parallel using two workers:

```powershell
python -m pytest tests/test_abs_module.py -n 2 -v
```

### Test Results

The recorded full test run reported **27 passed tests**.

The CSV-based test run reported **7 passed tests**, with the remaining tests deselected by the marker filter.

The parallel execution run also reported **27 passed tests**.

### Documentation

The Excel workbook in `docs/Test_Cases.xlsx` contains CSV-based test cases and an execution summary. The project setup demonstration video should also be added to the repository before final submission.

### Submission

Repository: https://github.com/Hunaiza-ct/SQE-Assignment-3

Before submission, verify the required module coverage, test design notes, configuration, setup video, repository visibility, and GCR submission.
