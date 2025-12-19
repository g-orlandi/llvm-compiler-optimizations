# LLVM Compiler Optimizations

Academic repository developed as part of a Compilers (II module) course during a BSc in Computer Science.

This repository collects multiple assignments focused on compiler analysis and optimization techniques, with particular emphasis on LLVM-based implementations, including custom optimization passes and data-flow analyses.

Group members:
- Luca Ballotti
- Francesco Mancuso
- Giovanni Orlandi

---

## Generating LLVM IR from C/C++ sources

To generate LLVM IR (.ll) files starting from C/C++ code:

### From .cpp to .ll

clang++ -Xclang -disable-O0-optnone -O0 -S -emit-llvm file_test.cpp -o file_test.ll

### Removing load and store instructions

opt -S -p file_test.ll -o file_test.m2r.ll

---

## Repository structure

### 01_assignment

Contains the implementation related to the first assignment.  
Detailed documentation is available inside the folder:

01_assignment/README.md

---

### 02_assignment

Contains the second assignment, consisting of a theoretical and practical analysis documented in:

02_assignment/dataflow_analysis.md

---

### 03_assignment

Contains the code and documentation for the third assignment.

03_assignment/README.md

---

### 04_assignment

Contains the implementation of the fourth assignment, including an LLVM optimization pass (loop fusion) and related test cases.

04_assignment/README.md

---

## Notes

This repository is intended as an academic project, showcasing applied compiler concepts such as:
- data-flow analysis
- LLVM IR manipulation
- optimization pass design
- correctness and convergence considerations

Individual assignments may vary in scope and level of completeness, reflecting the incremental structure of the course.
