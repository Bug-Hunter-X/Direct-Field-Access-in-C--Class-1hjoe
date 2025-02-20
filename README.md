# Direct Field Access Bug in C#

This repository demonstrates a common but subtle bug in C#: directly accessing a class field instead of using its associated property.  This can lead to maintainability issues and unexpected behavior.

## The Problem

The `bug.cs` file contains a class with a private field and a public property.  However, the `MyMethod` function accesses the private field directly, bypassing the property's setter.  This violates the principle of encapsulation and can lead to difficulties in maintaining and debugging the code.

## The Solution

The `bugSolution.cs` file shows the corrected code, where `MyMethod` consistently uses the property, maintaining proper encapsulation.  Using the property allows for the implementation of additional logic (validation, logging, etc.) within the setter without affecting other parts of the code that utilize the property.

## How to Reproduce

1. Clone this repository.
2. Compile and run `bug.cs`.  While it will compile and execute, the direct field access represents a bad practice.
3. Compare it with `bugSolution.cs` to understand the improved design.