# OpenMP Matrix Multiplication

This program demonstrates matrix multiplication in parallel using OpenMP, a standard for parallel programming in commonly used languages like C and C++.

## What is OpenMP?

OpenMP is a standard that defines a set of rules and directives for parallel programming in frequently used programming languages. By following this standard, developers can write programs that are compatible with different platforms offering OpenMP support.

## How does OpenMP differ from simple parallelization?

OpenMP offers several advantages over simple parallelization:

- **Simplified syntax:** OpenMP uses pragma directives and standard functions to identify parts of the code that can be executed in parallel. This makes it easier for programmers to integrate parallelization into their code compared to writing parallel code using other libraries.
  
- **Thread management:** OpenMP provides ready-to-use functions for creating and managing threads. Programmers don't have to write thread management code from scratch, as OpenMP makes this process easier and safer.
  
- **Automated synchronization:** OpenMP automates some aspects of synchronization necessary for parallel programs. For example, you can use the `critical` directive to ensure that only one thread has access to a certain part of the code at a time, or `barrier` to synchronize all threads at a specific point in the code.

## Job Description:

1. To use OpenMP, we first need to include the library: `#include<omp.h>`.
   
2. We use OpenMP to parallelize the inner loop where we perform matrix multiplication. We use `#pragma omp parallel for`, which allows the loop to be executed in parallel by OpenMP threads.
   
3. The code also utilizes `collapse(2)` to combine the two levels of loops into a single one. This allows all threads to share the work more efficiently, avoiding overhead created by multiplying two levels of loops. This is an optimization provided by OpenMP that improves program performance.
   
4. After the multiplication, the resulting matrix will be printed in the terminal.
