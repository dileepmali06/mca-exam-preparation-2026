# Module 1 -- Introduction to Artificial Intelligence

# Topic 1.1.5 -- Graph Search Algorithms

> **Source:** AI for Everyone (Amity University) -- Module 1

------------------------------------------------------------------------

# Learning Objectives

After completing this topic, you should be able to:

-   Define Graph Search Algorithms.
-   Understand Graph, Node, and Edge.
-   Explain Breadth First Search (BFS).
-   Explain Depth First Search (DFS).
-   Differentiate BFS and DFS.
-   Understand real-world applications of Graph Search.

------------------------------------------------------------------------

# 1. Introduction

Graph Search Algorithms are computational techniques used to traverse
and explore graphs to locate information or solve problems.

These algorithms are widely used in Artificial Intelligence, Robotics,
Navigation Systems, Social Networks, and Recommendation Systems.

------------------------------------------------------------------------

# 2. What is a Graph?

A Graph is a non-linear data structure consisting of:

-   Nodes (Vertices)
-   Edges (Connections)

Example:

``` text
        A
      /   \
     B     C
    / \     \
   D   E     F
```

Nodes:

A, B, C, D, E, F

Edges:

A-B

A-C

B-D

B-E

C-F

------------------------------------------------------------------------

# 3. Graph Search Algorithms

## Definition

> **Graph Search Algorithms are computational techniques used to
> traverse and explore graphs in order to locate information or solve
> problems.**

These algorithms systematically visit graph nodes to search for a target
or discover all reachable nodes.

------------------------------------------------------------------------

# 4. Breadth First Search (BFS)

## Definition

Breadth First Search is a graph traversal algorithm that visits all
neighboring nodes before moving to the next level.

------------------------------------------------------------------------

## Working

    Start Node
         │
    Visit Node
         │
    Add to Queue
         │
    Visit Neighbours
         │
    Repeat

Traversal Example

            A
          /   \
         B     C
        / \     \
       D   E     F

    Traversal:

    A → B → C → D → E → F

------------------------------------------------------------------------

## Characteristics

-   Level-by-level traversal
-   Uses Queue (FIFO)
-   Finds shortest path in unweighted graphs
-   Simple and systematic

------------------------------------------------------------------------

## Applications

-   Google Maps
-   Social Networks
-   GPS Navigation
-   Web Crawlers
-   Network Broadcasting

------------------------------------------------------------------------

# 5. Depth First Search (DFS)

## Definition

Depth First Search is a graph traversal algorithm that explores one
complete path before backtracking.

------------------------------------------------------------------------

## Working

    Start Node
         │
    Visit Node
         │
    Push into Stack
         │
    Move Deeper
         │
    Backtrack

Traversal Example

            A
          /   \
         B     C
        / \     \
       D   E     F

    Traversal:

    A → B → D → E → C → F

------------------------------------------------------------------------

## Characteristics

-   Depth-wise traversal
-   Uses Stack (LIFO)
-   Uses Backtracking
-   Suitable for maze solving

------------------------------------------------------------------------

## Applications

-   Maze Solving
-   File System Traversal
-   Puzzle Solving
-   Dependency Resolution

------------------------------------------------------------------------

# 6. BFS vs DFS

  Feature          BFS                    DFS
  ---------------- ---------------------- --------------------
  Full Form        Breadth First Search   Depth First Search
  Data Structure   Queue                  Stack
  Traversal        Level Wise             Depth Wise
  Path             Shortest Path          Deep Exploration
  Technique        FIFO                   LIFO

------------------------------------------------------------------------

# 7. AI Workflow

``` text
Problem

↓

Graph

↓

Search Algorithm

↓

Best Path

↓

Solution
```

------------------------------------------------------------------------

# 8. Real-World Applications

### Google Maps

Finds routes between locations.

### Facebook

Friend recommendations.

### LinkedIn

Professional connection search.

### Uber

Driver routing.

### Robot Navigation

Path planning.

### Games

Maze solving and path finding.

------------------------------------------------------------------------

# 9. Software Engineering Perspective

Graph Search Algorithms are widely used in:

-   Search Engines
-   Recommendation Systems
-   File Systems
-   Routing Algorithms
-   Social Media Platforms

Backend systems often rely on graph traversal techniques to process
connected data efficiently.

------------------------------------------------------------------------

# Quick Revision

-   Graph = Nodes + Edges
-   BFS = Level-wise traversal
-   DFS = Depth-wise traversal
-   BFS uses Queue
-   DFS uses Stack
-   Both are Graph Traversal Algorithms

------------------------------------------------------------------------

# Important Definitions

## Graph

A graph is a data structure consisting of nodes and edges.

## Node

A node represents a point or vertex in a graph.

## Edge

An edge is a connection between two nodes.

## BFS

Breadth First Search visits neighboring nodes first.

## DFS

Depth First Search explores one path completely before backtracking.

------------------------------------------------------------------------

# Important Keywords

-   Graph
-   Node
-   Edge
-   BFS
-   DFS
-   Queue
-   Stack
-   Graph Traversal
-   Path Finding
-   Backtracking

------------------------------------------------------------------------

# Frequently Asked University Questions

## 2 Marks

1.  Define Graph.
2.  Define BFS.
3.  Define DFS.

## 5 Marks

1.  Explain Graph Search Algorithms.
2.  Explain Breadth First Search.
3.  Explain Depth First Search.

## Long Answer

1.  Differentiate BFS and DFS.
2.  Explain Graph Traversal with diagrams.

------------------------------------------------------------------------

# MCQs

### 1. A Graph consists of:

A. Rows and Columns

**B. Nodes and Edges ✅**

C. Arrays

D. Objects

------------------------------------------------------------------------

### 2. BFS stands for:

A. Binary First Search

**B. Breadth First Search ✅**

C. Branch First Search

D. Basic First Search

------------------------------------------------------------------------

### 3. DFS stands for:

A. Direct First Search

**B. Depth First Search ✅**

C. Data First Search

D. Double First Search

------------------------------------------------------------------------

### 4. BFS uses:

A. Stack

**B. Queue ✅**

C. Heap

D. Tree

------------------------------------------------------------------------

### 5. DFS uses:

A. Queue

**B. Stack ✅**

C. Graph

D. Heap

------------------------------------------------------------------------

### 6. BFS explores:

A. Randomly

**B. Level by Level ✅**

C. Backwards

D. Depth First

------------------------------------------------------------------------

### 7. DFS explores:

A. Level Wise

**B. One Path Completely ✅**

C. Randomly

D. Breadth Wise

------------------------------------------------------------------------

### 8. Which algorithm is commonly used in maze solving?

A. BFS

**B. DFS ✅**

C. Binary Search

D. Linear Search

------------------------------------------------------------------------

### 9. Google Maps uses Graph Search Algorithms for:

A. Image Editing

**B. Route Finding ✅**

C. Music Streaming

D. Video Rendering

------------------------------------------------------------------------

### 10. Which statement is correct?

A. BFS uses Stack.

B. DFS uses Queue.

**C. BFS uses Queue while DFS uses Stack. ✅**

D. BFS and DFS are identical.

------------------------------------------------------------------------

# One-Line Summary

Graph Search Algorithms systematically explore connected nodes to find
information, discover paths, and solve complex problems in Artificial
Intelligence.
