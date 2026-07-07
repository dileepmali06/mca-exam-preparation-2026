# Module 2 -- Artificial Intelligence with Python

# Lesson 2

## 2.1.4 -- Overview and Components of Constraint Satisfaction Algorithm (CSP)

> **Source:** AI for Everyone (MCA Semester III)

------------------------------------------------------------------------

# Learning Objectives

After completing this lesson, you should be able to:

-   Define Constraint Satisfaction Problem (CSP).
-   Explain why CSP is important in AI.
-   Understand Variables, Domains, and Constraints.
-   Explain Constraint Graphs and Backtracking.
-   Describe real-world applications of CSP.

------------------------------------------------------------------------

# Introduction

Many Artificial Intelligence problems require finding a valid solution
while satisfying a set of rules.

Constraint Satisfaction Problems (CSPs) provide a structured way to
solve such problems efficiently.

------------------------------------------------------------------------

# Why CSP?

Real-world examples include:

-   Timetable Scheduling
-   Sudoku
-   Map Coloring
-   Flight Scheduling
-   Resource Allocation
-   Doctor Shift Planning

The goal is to satisfy every rule while finding a valid solution.

------------------------------------------------------------------------

# Definition

> **A Constraint Satisfaction Problem (CSP) is a problem in which values
> are assigned to variables while satisfying a set of constraints.**

------------------------------------------------------------------------

# Components of CSP

## 1. Variables

Variables are entities that require values.

Example:

-   AI Exam
-   Python Exam
-   DBMS Exam

------------------------------------------------------------------------

## 2. Domain

A Domain is the set of all possible values for a variable.

Example:

``` text
{Monday, Tuesday, Wednesday}
```

------------------------------------------------------------------------

## 3. Constraints

Constraints are rules that restrict valid assignments.

Example:

``` text
AI Exam ≠ Python Exam
```

------------------------------------------------------------------------

# CSP Workflow

``` text
Variables
     │
Domains
     │
Constraints
     │
Valid Solution
```

------------------------------------------------------------------------

# Constraint Graph

Nodes represent variables.

Edges represent constraints.

Example:

``` text
AI ------- Python
 \         /
   \     /
     DBMS
```

------------------------------------------------------------------------

# Backtracking Search

Backtracking is the most common technique used to solve CSPs.

Workflow:

``` text
Choose Variable
      │
Assign Value
      │
Constraint Satisfied?
      │
YES → Next Variable
NO  → Backtrack
```

------------------------------------------------------------------------

# Real-World Applications

-   Sudoku Solver
-   University Timetable
-   Airline Scheduling
-   Hospital Shift Planning
-   Warehouse Resource Allocation
-   Robot Task Planning

------------------------------------------------------------------------

# Software Engineering Perspective

Examples:

-   Appointment Booking Systems
-   Employee Scheduling Software
-   Meeting Room Allocation
-   Cloud Resource Scheduling

Backend systems use CSP logic to generate valid assignments while
satisfying business rules.

------------------------------------------------------------------------

# Advantages

-   Efficient rule-based problem solving
-   Handles complex scheduling problems
-   Finds valid solutions systematically
-   Widely used in planning applications

------------------------------------------------------------------------

# Limitations

-   Large CSPs become computationally expensive
-   Constraint design can be difficult
-   Some problems require optimization techniques

------------------------------------------------------------------------

# Quick Revision

-   CSP = Variables + Domains + Constraints
-   Goal = Valid Assignment
-   Constraint Graph = Variable relationships
-   Backtracking = Common solving technique

------------------------------------------------------------------------

# Important Definitions

## Constraint Satisfaction Problem

Assign values to variables while satisfying constraints.

## Variable

An entity that needs a value.

## Domain

The set of possible values.

## Constraint

A rule limiting assignments.

## Backtracking

A search technique that revisits previous choices when constraints fail.

------------------------------------------------------------------------

# Important Keywords

-   CSP
-   Variable
-   Domain
-   Constraint
-   Constraint Graph
-   Backtracking
-   Scheduling
-   Planning
-   Sudoku
-   Map Coloring

------------------------------------------------------------------------

# Frequently Asked University Questions

## 2 Marks

1.  Define CSP.
2.  What is a Domain?
3.  What is a Constraint?

## 5 Marks

1.  Explain the components of CSP.
2.  Explain Backtracking in CSP.

## Long Answer

1.  Explain Constraint Satisfaction Problems with suitable examples.
2.  Discuss applications of CSP in Artificial Intelligence.

------------------------------------------------------------------------

# Exam Tips

For maximum marks:

1.  Write the definition.
2.  Explain Variables, Domains, and Constraints.
3.  Draw the CSP workflow.
4.  Explain Backtracking.
5.  Mention practical applications.

------------------------------------------------------------------------

# MCQs

### Q1. A CSP consists of:

A. Variables, Domains, and Constraints

B. Arrays and Loops

C. HTML and CSS

D. CPU and RAM

**Answer:** A. Variables, Domains, and Constraints

**Explanation:** These are the three core components of every CSP.

------------------------------------------------------------------------

### Q2. A Domain represents:

A. Source Code

B. Possible values of a variable

C. Database

D. Compiler

**Answer:** B. Possible values of a variable

**Explanation:** A domain contains all valid values for a variable.

------------------------------------------------------------------------

### Q3. A Constraint is:

A. A Rule

B. A Loop

C. A Function

D. A Class

**Answer:** A. A Rule

**Explanation:** Constraints restrict possible assignments.

------------------------------------------------------------------------

### Q4. Which algorithm is commonly used to solve CSP?

A. Bubble Sort

B. Backtracking

C. Merge Sort

D. Binary Search

**Answer:** B. Backtracking

**Explanation:** Backtracking explores assignments until a valid
solution is found.

------------------------------------------------------------------------

### Q5. Sudoku is an example of:

A. CSP

B. Database

C. Networking

D. Compiler

**Answer:** A. CSP

**Explanation:** Sudoku requires satisfying multiple constraints.

------------------------------------------------------------------------

### Q6. In a Constraint Graph, nodes represent:

A. Variables

B. Files

C. Programs

D. CPUs

**Answer:** A. Variables

**Explanation:** Each node corresponds to one variable.

------------------------------------------------------------------------

### Q7. Which is a CSP application?

A. Timetable Scheduling

B. Hospital Scheduling

C. Flight Scheduling

D. All of the Above

**Answer:** D. All of the Above

**Explanation:** CSP is widely used in scheduling and planning.

------------------------------------------------------------------------

### Q8. If a constraint fails, Backtracking:

A. Stops forever

B. Tries another assignment

C. Deletes the variable

D. Restarts the system

**Answer:** B. Tries another assignment

**Explanation:** It returns to a previous step and explores another
value.

------------------------------------------------------------------------

### Q9. The goal of CSP is:

A. Find a valid solution satisfying all constraints

B. Compress files

C. Edit images

D. Create databases

**Answer:** A. Find a valid solution satisfying all constraints

**Explanation:** Every constraint must be satisfied.

------------------------------------------------------------------------

### Q10. Which statement is correct?

A. CSP ignores rules.

B. CSP uses Variables, Domains, and Constraints to find valid solutions.

C. CSP is only used in games.

D. CSP cannot solve scheduling problems.

**Answer:** B. CSP uses Variables, Domains, and Constraints to find
valid solutions.

**Explanation:** This is the fundamental idea behind CSP.

------------------------------------------------------------------------

# One-Line Summary

Constraint Satisfaction Problems help AI find valid solutions by
assigning values to variables while satisfying all defined constraints.
