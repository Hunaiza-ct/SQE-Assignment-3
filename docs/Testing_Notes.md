\# Unit Testing Design Notes



\## Project

TheAlgorithms/Python — Software Quality Engineering Assignment



\## Selected Module

`maths.abs`



\## 1. Functions Under Test



\- `abs\_val`

\- `abs\_min`

\- `abs\_max`

\- `abs\_max\_sort`



\## 2. Equivalence Class Partitioning (ECP)



\### abs\_val

Input classes:

\- Negative numbers: expected output is the positive magnitude.

\- Positive numbers: expected output is unchanged.

\- Zero: expected output is zero.

\- Decimal numbers: expected output is the positive magnitude.



\### abs\_min

Input classes:

\- Non-empty lists containing positive numbers.

\- Non-empty lists containing negative numbers.

\- Lists containing both positive and negative numbers.

\- Lists containing zero.

\- Empty lists: expected to raise `ValueError`.



\### abs\_max

Input classes:

\- Non-empty lists containing positive numbers.

\- Non-empty lists containing negative numbers.

\- Lists containing both positive and negative numbers.

\- Lists containing zero.

\- Empty lists: expected to raise `ValueError`.



\### abs\_max\_sort

Input classes:

\- Non-empty lists containing positive numbers.

\- Non-empty lists containing negative numbers.

\- Lists containing both positive and negative numbers.

\- Lists containing zero.

\- Empty lists: expected to raise `ValueError`.



\## 3. Boundary Value Analysis (BVA)



The following boundary-oriented inputs are considered:

\- Zero (`0`).

\- Values immediately below and above zero, such as `-1` and `1`.

\- Small decimal values, such as `-3.5` and `2.5`.

\- Larger magnitude values, such as `-100` and `12`.

\- Empty lists for functions that require a non-empty list.



\## 4. Parameterized Testing



Parameterized tests execute the same test function with multiple input and expected-output pairs. This reduces duplicated test code and makes it easier to cover different input classes.



\## 5. CSV-Based Data-Driven Testing



The file `test\_data/abs\_test\_data.csv` provides numeric inputs and expected absolute values. The tests read the CSV data and execute `abs\_val` for each row.



\## 6. Exception Testing



The empty-list tests check that `abs\_min`, `abs\_max`, and `abs\_max\_sort` raise `ValueError`.



\## 7. Scope and Limitations



These notes describe the test design for `maths.abs`. Additional modules must be selected and documented separately to satisfy the assignment requirement for three different modules.

