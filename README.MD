# ESEP Grade Calculator

A Go library that calculates a student's final letter grade from three kinds of grades: assignments, exams, and essays.

## How grades are calculated

1. Average each category separately.
2. Combine the averages using weights: Assignments 50%, Exams 35%, Essays 15%.
3. Convert to a letter: A ≥ 90, B ≥ 80, C ≥ 70, D ≥ 60, otherwise F. Passing requires a C or better.

## Requirements

- Go 1.24+ (check with `go version`).

## Project structure

- `grade-calculator/go.mod`: module definition and Go version
- `grade-calculator/grade_calculator.go`: library code
- `grade-calculator/grade_calculator_test.go`: unit tests

## Running tests

All commands run from the `grade-calculator/` folder

```bash
cd grade-calculator
go test -v ./...
```

## Code coverage

```bash
go test -cover ./...                         # quick percentage
go test -coverprofile=coverage.txt ./...     # write a coverage report
```