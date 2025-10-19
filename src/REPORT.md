# Project Report: s21_decimal

This document provides instructions on how to run, test, and analyze the `s21_decimal` project.

## How to Run the Project

The project uses a `Makefile` to manage building and testing. All commands should be run from the `src` directory.

### Building the Library

To build the static library `s21_decimal.a`, run the following command:

```bash
make all
```

This will compile the source files in `src/components` and create the library file `s21_decimal.a` in the `src` directory.

### Running Tests

To compile and run the unit tests, use the following command:

```bash
make test
```

This will compile the test files and the library, create a test executable, and run it.

## Code Coverage

The project is configured to generate a code coverage report using `gcov` and `lcov`.

To generate the report, run:

```bash
make gcov_report
```

This command will first run the tests with coverage flags, then generate an HTML report in the `src/html_report` directory.

To view the report, open the following file in a web browser:

```
src/html_report/index.html
```

## Memory Leak Check

Memory leak checking is performed using `valgrind`.

To run the tests with `valgrind` and check for memory leaks, use the following command:

```bash
make valgrind
```

The output will include a summary of any memory leaks found.
