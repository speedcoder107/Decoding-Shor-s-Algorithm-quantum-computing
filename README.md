# Shor's Algorithm Implementation: From Basics to Quantum Factoring

This project provides an in-depth explanation of Shor's Algorithm, starting from the foundational mathematics, building up key quantum algorithms such as Quantum Fourier Transform (QFT) and Quantum Phase Estimation (QPE), and finally demonstrating the complete implementation of Shor's algorithm for integer factorization. 

## Overview

- bullet point 1
* bullet point 2

Shor's Algorithm is a quantum algorithm that efficiently factors large integers. It is based on the principle that quantum computers can perform certain operations much faster than classical computers, providing a polynomial-time solution to the problem of integer factorization, which is otherwise considered intractable for large numbers.

This project walks you through the following topics:

1. **Understading Shor's Algorithm Mathematically**: Understanding the mathematical background necessary for Shor's algorithm, including modular exponentiation and finding the period of a function.
   
2. **Implementing Shor's Algorithm Classically**: Helps understanding the execution of Shor's algorithm classically for small numbers and it's comparison with Quantum implimentation.
   
4. **Quantum Fourier Transform (QFT)**: An essential quantum operation that is a key component of Shor’s algorithm, used to extract periodicity information from quantum states.
   
5. **Quantum Phase Estimation (QPE)**: A quantum algorithm used to estimate the phase of a quantum state, which plays a crucial role in finding the period of modular exponentiation in Shor's algorithm.

6. **Shor's Algorithm for Integer Factorization**: The complete quantum algorithm that uses the aforementioned techniques to efficiently factor integers.

## Structure of the Project

The project is organized in a Jupyter Notebook, which is divided into the following sections:

### 1. **Implementing Shor's Algorithm Mathematically**
   - **Modular Exponentiation**: The core mathematical operation in Shor's algorithm, where we need to calculate powers of a number modulo \( N \). This process is essential for exploring how the algorithm determines the period of a function.
   - **Periodicity and Finding the Period**: The primary goal is to find the smallest period \( r \) such that \( a^r \mod N = 1 \), for a randomly chosen \( a \). This period is the key to factoring \( N \).
   - **Why the Period Matters**: The periodicity provides us with crucial information that allows us to factorize the integer \( N \) by using the properties of the greatest common divisor (GCD).
   - **Classical Approach to Find the Period**: This section includes a basic implementation of classical techniques to compute the period \( r \) of the function \( a^x \mod N \) using brute force, and highlights the computational difficulties when \( N \) is large.

### 2. **Implementing Shor's Algorithm Classically**
   - **Finding the Period \( r \)**: The classical method for finding the period of \( a^x \mod N \) involves brute-force testing of powers of \( a \) until we find the smallest \( r \) such that \( a^r \mod N = 1 \). This is a computationally expensive process for large numbers, especially when \( N \) is large, making it infeasible for classical computers to factor large numbers efficiently.
   - **Limitations of Classical Methods**: Classical methods for determining the period of modular exponentiation suffer from inefficiencies and exponential scaling as the size of \( N \) increases. This makes it impractical for factoring large numbers, such as those used in modern cryptography (RSA encryption).
   - **Comparison to Quantum Approach**: The classical method of finding the period is contrasted with the quantum approach used in Shor’s algorithm, where quantum phase estimation (QPE) and quantum Fourier transform (QFT) allow the period to be found exponentially faster. This section lays the groundwork for understanding how Shor's algorithm overcomes the computational barriers posed by classical methods.

### 2. **Quantum Fourier Transform (QFT)**
   - Introduction to the concept of QFT.
   - Step-by-step guide on how to implement QFT on a quantum computer.
   - Visualization and explanation of the QFT algorithm.

### 3. **Quantum Phase Estimation (QPE)**
   - Overview of QPE and its role in Shor's algorithm.
   - Explanation of how QPE estimates the phase of a quantum state and its application to find the period of a function.
   - Code for implementing QPE on a quantum computer.

### 4. **Shor's Algorithm**
   - Complete implementation of Shor's algorithm for integer factorization.
   - Explanation of how QPE is used within Shor's algorithm.
   - Example of using Shor’s algorithm to factor the number 15 and other numbers.

### 5. **Simulating the Algorithm**
   - Code to simulate Shor's algorithm using Qiskit.
   - Visualization of quantum circuits and results.
   - Classical post-processing steps to compute the factors.

