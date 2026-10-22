# Bug Fixing with Python and AI

A Python debugging project that uses `unittest` and the RED → FIX → GREEN cycle to find, understand, and fix bugs in student utility functions.

## Features

- Calculates the average of student marks
- Checks whether a student has passed
- Assigns grades: Fail, Second, First, or Distinction
- Includes 9 automated unit tests
- Documents the failing RED stage and the passing GREEN stage

## Files

- `student_utils.py` — Corrected Python functions
- `test_student_utils.py` — Unit tests for the functions
- `red_output.txt` — Test output before the fixes
- `green_output.txt` — Test output after the fixes

## Bugs Fixed

1. Average calculation divided by `len(marks) - 1` instead of `len(marks)`.
2. A mark of `40` was incorrectly treated as failing.
3. The Distinction condition was checked after the First condition.

## Run the Tests

```bash
python test_student_utils.py
```

## Final Result

All 9 tests pass successfully.

```text
.........
----------------------------------------------------------------------
Ran 9 tests in 0.001s

OK
```

## RED → FIX → GREEN

- **RED:** Run tests against buggy code and observe failures.
- **FIX:** Correct the implementation without weakening the tests.
- **GREEN:** Run the same tests again until all pass.
