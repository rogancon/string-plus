# s21_string+ (Completed Project)

This repository holds the finished implementation of the custom `string.h` library along with extended functionalities such as custom `sprintf` and `sscanf` functions and additional string processing utilities. The project was completed following the C11 standard and Google C Style guidelines.

## Project Overview

This project started as an assignment to recreate the standard C library functions related to string handling without directly using the standard implementations. It has evolved into a robust, fully-tested library that not only replicates standard functions but also introduces new features inspired by string handling in other programming languages like C#.

### Key Objectives Achieved

- **Custom String Library Implementation:** All standard `string.h` functions (e.g., `memchr`, `memcmp`, `memcpy`, `strlen`, etc.) are implemented with a focus on error handling and memory safety.
- **Extended Formatting Functions:** Both `sprintf` and `sscanf` functions have been reimplemented to support a broad range of format specifiers, flags, width/precision modifiers, and length modifiers.
- **Bonus Features:** Additional formatting modifiers (such as `%g`, `%e`, `%x`, etc.) for `sprintf`, full support for `sscanf`, and special string processing functions (`to_upper`, `to_lower`, `insert`, `trim`) have been successfully added.
- **Static Library Creation:** The final product is built as a static library (`s21_string.a`) for seamless integration with other C projects.
- **Rigorous Testing:** Comprehensive unit tests using the Check framework cover at least 80% of each function, ensuring the implementation behaves consistently with the standard library.
- **Code Coverage Reporting:** A Makefile target is provided to generate an HTML gcov report for code coverage, further demonstrating the robustness of the testing suite.

## Features

- **Full Implementation of Core String Functions:** All key operations, such as string copying, concatenation, comparison, tokenization, and search, are implemented manually.
- **Custom `sprintf` and `sscanf` Functions:** These functions support a wide array of specifiers (`c`, `d`, `f`, `s`, `u`, `%`, etc.), flags (such as `-`, `+`, and space), and modifiers (width, precision, and length).
- **Extended Format Specifiers:** Bonus features include support for additional specifiers like `%g`, `%e`, `%x`, `%o`, `%p` along with extra flags (`#`, `0`) and dynamic width/precision (`*`, `.*`).
- **Special String Processing Functions:** Functions for converting strings to upper or lower case, inserting substrings, and trimming characters from the beginning or end of strings add extra utility beyond the standard library.
- **Structured, Readable Code:** The project is organized according to modern C practices, emphasizing maintainability, code reuse, and adherence to the POSIX.1-2017 standard.

## Project Structure

- **`src/`**  
  Contains all the source files for the library functions and unit tests.
  
- **`include/`**  
  Header files including `s21_string.h`, which exposes the API for the library.
  
- **`tests/`**  
  Unit tests written using the Check framework to verify functionality and edge cases.
  
- **`Makefile`**  
  Provides targets to build the library (`s21_string.a`), run tests, clean build artifacts, and generate gcov reports.
  
- **`gcov_report/`**  
  Directory where the HTML code coverage report is generated when using the `gcov_report` target.

## Build and Test Instructions

1. **Build the Static Library:**
   ```sh
   make s21_string.a
   ```
2. **Run Unit Tests:**
   ```sh
   make test
   ```
3. **Generate Code Coverage Report:**
   ```sh
   make gcov_report
   ```
   This will run the tests with gcov flags and generate an HTML report in the `gcov_report/` directory.

## Technical Details

- **Language & Standard:** Implemented in C using the C11 standard.
- **Compiler:** Developed and tested with GCC.
- **Coding Style:** Follows Google C Style guidelines.
- **Memory Management:** Careful attention was paid to proper memory handling and error checking, ensuring stability even in edge cases.
- **Platform-Specific Implementation:** Custom error message arrays have been implemented for different platforms as per the project requirements (instead of relying on system arrays like `sys_errlist`).

## Conclusion

This completed project is a comprehensive reimplementation of the string handling functions traditionally found in `string.h`, with significant enhancements in formatting and processing capabilities. It is designed for educational purposes and can serve as a robust foundation for understanding how these core C functions operate under the hood.

