# Welcome to Gift Store!
This is where you can start to get familiar with the problem and what you need to run it.
This codebase is used during code pairing session for JOI initiative.
It's focused on identifying code smells, refactoring and testing legacy codebase while promoting conversations.

## Problem Statement
A college student with a group of friends enjoys giving gifts tailored to each person's interests. He/She frequents a gift shop that offers a wide range of transaction. Could you assist him/her in calculating his/her expenditure on gifts?
5% GST gets added on total worth of products.<br>
NOTE1:- Make sure to handle exceptions gracefully.<br>
NOTE2:- Make sure to write modular code.<br>
For more info refer to the problem statement document shared to you separately.

## Technologies used
- C++14 or above
- CMake - build tool
- [Googletest - unit testing framework](https://google.github.io/googletest/)

## What you need to run it
- C++ Compiler
- [Cmake](https://cgold.readthedocs.io/en/latest/first-step/installation.html)

## Before the interview
Get familiar with the codebase! Make sure you have the necessary dependencies installed, and that you are able to run the tests.

## Build
#### Note: Run the below command only when the tests are fixed.
```console
call buildapp.bat
```

## Run Tests
#### Note: Initially the tests will fail. You need to fix them.
```console
cd build
GiftStoreAppTest.exe
cd ..
```

## Run the Application
To understand how this application would be used you can check the `main` method in the `src/GiftStore.cpp`. If you want to see the results, run:
```console
cd build
GiftStoreApp.exe
cd ..
```

## Existing Implementation
Application code currently has the following implementation:
- Required Domain Models needed for the base problem statement.
- Hard-coded list of gift items with their prices.
- A function to calculate the total cost of gifts (stubbed to add the core logic on your own).