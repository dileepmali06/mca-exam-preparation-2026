# Module 1 -- Introduction to Artificial Intelligence

# Topic 1.1.4 -- Introduction to Search Algorithms

> **Source:** AI for Everyone (Amity University) -- Module 1

------------------------------------------------------------------------

# Learning Objectives

After completing this topic, you should be able to:

-   Define Search Algorithms.
-   Explain why Search Algorithms are important in AI.
-   Differentiate Sequential Search and Interval Search.
-   Understand Linear Search and Binary Search.
-   Identify real-world applications of Search Algorithms.

------------------------------------------------------------------------

# 1. Introduction

Artificial Intelligence systems frequently need to search for
information, solutions, or optimal decisions.

A Search Algorithm is a systematic procedure used to locate a desired
element or determine the best solution from a collection of possible
choices.

Search Algorithms are fundamental to AI because intelligent systems
constantly search for the best action before making decisions.

------------------------------------------------------------------------

# 2. Why Search Algorithms are Needed

Many AI problems have multiple possible solutions.

Examples:

-   Finding the shortest route in Google Maps
-   Finding the best chess move
-   Searching products on Amazon
-   Searching songs on Spotify
-   Searching information on Google

Instead of checking randomly, AI uses Search Algorithms to efficiently
find the best result.

------------------------------------------------------------------------

# 3. Definition

> **A Search Algorithm is a step-by-step procedure used to locate a
> desired element or determine the best solution from a collection of
> possible choices.**

------------------------------------------------------------------------

# 4. Types of Search Algorithms

According to the syllabus, Search Algorithms are broadly classified
into:

## Sequential Search

Also known as **Linear Search**.

Characteristics:

-   Checks elements one by one.
-   Works on both sorted and unsorted data.
-   Easy to implement.
-   Suitable for small datasets.

Example:

    5 → 10 → 20 → 30 → Found

------------------------------------------------------------------------

## Interval Search

Interval Search works on **sorted datasets**.

The most common Interval Search algorithm is **Binary Search**.

Characteristics:

-   Starts from the middle element.
-   Eliminates half of the remaining search space after every
    comparison.
-   Much faster than Linear Search for sorted data.

Example:

    5 10 15 20 25 30 35 40

    Middle = 20

    Target = 35

    Search Right Half

    Found

------------------------------------------------------------------------

# 5. Linear Search vs Binary Search

  Feature            Linear Search         Binary Search
  ------------------ --------------------- -------------------
  Data Requirement   Sorted or Unsorted    Sorted Only
  Method             Sequential Checking   Divide and Search
  Speed              Slower                Faster
  Complexity         O(n)                  O(log n)

------------------------------------------------------------------------

# 6. AI Search Workflow

    Problem
       │
    Possible Solutions
       │
    Search Algorithm
       │
    Best Solution
       │
    Output

------------------------------------------------------------------------

# 7. Real-World Applications

## Google Maps

Uses Search Algorithms to identify the fastest route.

## Chess AI

Searches multiple possible moves before selecting the best one.

## Amazon

Searches millions of products and returns relevant results.

## Netflix

Searches and recommends relevant content.

## Medical Diagnosis

Searches possible diseases based on symptoms.

------------------------------------------------------------------------

# 8. Software Engineering Perspective

Search Algorithms are widely used in modern software:

-   Database Searching
-   Search Engines
-   E-commerce Websites
-   Recommendation Systems
-   Navigation Systems
-   File Searching

Backend developers use optimized searching techniques to improve
application performance.

------------------------------------------------------------------------

# Quick Revision

-   Search Algorithm = Method to find data or solutions.
-   Linear Search = One-by-one searching.
-   Binary Search = Middle-first searching.
-   Binary Search requires sorted data.
-   Search Algorithms are essential in AI decision making.

------------------------------------------------------------------------

# Important Definitions

## Search Algorithm

A step-by-step procedure used to find an element or determine the best
solution.

## Linear Search

A sequential searching technique that checks every element until the
desired element is found.

## Binary Search

A searching technique that repeatedly divides a sorted dataset into
halves until the target element is found.

------------------------------------------------------------------------

# Important Keywords

-   Search Algorithm
-   Linear Search
-   Binary Search
-   Sequential Search
-   Interval Search
-   Search Space
-   Dataset
-   Decision Making
-   Problem Solving
-   Path Finding

------------------------------------------------------------------------

# Frequently Asked University Questions

## 2 Marks

1.  Define Search Algorithm.
2.  What is Linear Search?
3.  What is Binary Search?

## 5 Marks

1.  Explain Search Algorithms.
2.  Differentiate Linear Search and Binary Search.

## Long Answer

1.  Explain Search Algorithms with suitable examples.
2.  Discuss Sequential Search and Interval Search.

------------------------------------------------------------------------

# MCQs

1.  Search Algorithms are used to:
    -   A. Increase RAM
    -   **B. Find data or solutions ✅**
    -   C. Format disks
    -   D. Play music
2.  Linear Search is also known as:
    -   A. Graph Search
    -   **B. Sequential Search ✅**
    -   C. DFS
    -   D. BFS
3.  Binary Search requires:
    -   A. Random Data
    -   **B. Sorted Data ✅**
    -   C. Images
    -   D. Internet
4.  Which search checks elements one by one?
    -   A. Binary Search
    -   **B. Linear Search ✅**
    -   C. DFS
    -   D. BFS
5.  Binary Search starts from:
    -   A. First Element
    -   **B. Middle Element ✅**
    -   C. Last Element
    -   D. Random Element
6.  Which search is generally faster?
    -   A. Linear Search
    -   **B. Binary Search ✅**
    -   C. Manual Search
    -   D. Sequential Search
7.  Google Maps uses Search Algorithms for:
    -   A. Video Streaming
    -   **B. Route Finding ✅**
    -   C. Audio Editing
    -   D. Printing
8.  Which is an example of Interval Search?
    -   A. Linear Search
    -   **B. Binary Search ✅**
    -   C. DFS
    -   D. BFS
9.  Search Algorithms are important in:
    -   A. AI
    -   B. Databases
    -   C. Search Engines
    -   **D. All of the Above ✅**
10. Search Algorithms help AI in:
    -   A. Decision Making
    -   B. Path Finding
    -   C. Problem Solving
    -   **D. All of the Above ✅**

------------------------------------------------------------------------

# One-Line Summary

Search Algorithms enable AI systems to efficiently locate information,
explore possible solutions, and choose the best action for solving
real-world problems.
