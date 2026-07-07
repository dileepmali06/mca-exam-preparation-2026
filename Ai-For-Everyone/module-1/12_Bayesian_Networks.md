# Module 1 -- Introduction to Artificial Intelligence

# Topic 1.3.2 -- Bayesian Networks

> **Source:** AI for Everyone (Amity University) -- Module 1

------------------------------------------------------------------------

# Learning Objectives

After completing this topic, you should be able to:

-   Define Bayesian Networks.
-   Explain why Bayesian Networks are used in AI.
-   Understand Nodes, Edges, and Conditional Probability.
-   Explain Directed Acyclic Graph (DAG).
-   Describe real-world applications of Bayesian Networks.

------------------------------------------------------------------------

# Introduction

Artificial Intelligence often works with uncertain information. Bayesian
Networks combine **Probability Theory** and **Graph Theory** to model
uncertainty and make intelligent predictions.

------------------------------------------------------------------------

# Why Bayesian Networks?

Traditional rule-based systems struggle when information is incomplete
or uncertain.

Bayesian Networks allow AI to:

-   Represent uncertain knowledge
-   Model dependencies between variables
-   Predict outcomes using probability

------------------------------------------------------------------------

# Definition

> **A Bayesian Network is a probabilistic graphical model that
> represents random variables and their conditional dependencies using a
> Directed Acyclic Graph (DAG).**

------------------------------------------------------------------------

# Components

## 1. Nodes

Nodes represent random variables.

Examples:

-   Clouds
-   Rain
-   Umbrella

------------------------------------------------------------------------

## 2. Edges

Edges represent dependencies between variables.

Example:

``` text
Clouds
   │
   ▼
Rain
   │
   ▼
Umbrella
```

------------------------------------------------------------------------

## 3. Conditional Probability

Conditional Probability represents the probability of an event given
another event.

Example:

``` text
P(Rain | Clouds)
```

------------------------------------------------------------------------

# Directed Acyclic Graph (DAG)

A Bayesian Network is represented using a Directed Acyclic Graph.

Characteristics:

-   Directed edges
-   No cycles
-   Parent-child relationships

Example:

``` text
Clouds
   │
   ▼
Rain
   │
   ▼
Umbrella
```

------------------------------------------------------------------------

# Working of Bayesian Networks

``` text
Evidence
    │
Conditional Probability
    │
Bayesian Network
    │
Inference
    │
Prediction
```

------------------------------------------------------------------------

# Medical Diagnosis Example

``` text
Disease
   │
   ▼
Fever
   │
   ▼
Cough
```

Given symptoms, AI calculates the probability of disease.

------------------------------------------------------------------------

# AI Applications

-   Medical Diagnosis
-   Fraud Detection
-   Spam Filtering
-   Recommendation Systems
-   Robotics
-   Autonomous Vehicles
-   Risk Analysis

------------------------------------------------------------------------

# Software Engineering Perspective

Developers use Bayesian Networks in:

-   Decision Support Systems
-   Fraud Detection APIs
-   Healthcare Applications
-   Recommendation Engines
-   Predictive Analytics

Example:

``` text
Salary
Credit Score
Loan History
      │
Bayesian Network
      │
Loan Approval Probability
```

------------------------------------------------------------------------

# Advantages

-   Handles uncertainty
-   Supports intelligent prediction
-   Represents dependencies
-   Improves decision making
-   Easy graphical representation

------------------------------------------------------------------------

# Limitations

-   Requires probability estimation
-   Complex for very large networks
-   Model building can be time-consuming

------------------------------------------------------------------------

# Quick Revision

-   Bayesian Network = Probability + Graph
-   Uses DAG
-   Nodes = Variables
-   Edges = Dependencies
-   Conditional Probability = Relationship between variables

------------------------------------------------------------------------

# Important Definitions

## Bayesian Network

A probabilistic graphical model using DAG.

## Node

Represents a random variable.

## Edge

Represents dependency between variables.

## DAG

Directed Acyclic Graph with no cycles.

## Conditional Probability

Probability of an event given another event.

------------------------------------------------------------------------

# Important Keywords

-   Bayesian Network
-   DAG
-   Node
-   Edge
-   Conditional Probability
-   Probability
-   Inference
-   Prediction
-   Uncertainty
-   Graphical Model

------------------------------------------------------------------------

# Frequently Asked University Questions

## 2 Marks

1.  Define Bayesian Network.
2.  What is DAG?
3.  Define Conditional Probability.

## 5 Marks

1.  Explain Bayesian Networks.
2.  Explain the components of Bayesian Networks.

## Long Answer

1.  Explain Bayesian Networks with suitable diagrams.
2.  Discuss applications of Bayesian Networks in AI.

------------------------------------------------------------------------

# Exam Tips

For maximum marks:

1.  Write the definition.
2.  Draw the DAG.
3.  Explain Nodes, Edges, and Conditional Probability.
4.  Explain working.
5.  Mention at least three applications.

------------------------------------------------------------------------

# MCQs

### Q1. Bayesian Networks combine:

A. Graph Theory and Probability Theory

B. HTML and CSS

C. Database and Networking

D. Compiler and Interpreter

**Answer:** A. Graph Theory and Probability Theory

**Explanation:** Bayesian Networks combine graph structures with
probability.

------------------------------------------------------------------------

### Q2. Bayesian Networks are represented using:

A. Binary Tree

B. Directed Acyclic Graph (DAG)

C. Circular Graph

D. Linked List

**Answer:** B. Directed Acyclic Graph (DAG)

**Explanation:** DAG is the standard representation.

------------------------------------------------------------------------

### Q3. A node represents:

A. Random Variable

B. File

C. Database

D. CPU

**Answer:** A. Random Variable

**Explanation:** Nodes correspond to variables.

------------------------------------------------------------------------

### Q4. An edge represents:

A. Program

B. Dependency

C. Folder

D. Memory

**Answer:** B. Dependency

**Explanation:** Edges indicate conditional dependence.

------------------------------------------------------------------------

### Q5. DAG stands for:

A. Directed Acyclic Graph

B. Data Analysis Graph

C. Dynamic AI Graph

D. Digital Access Graph

**Answer:** A. Directed Acyclic Graph

**Explanation:** DAG contains directed edges without cycles.

------------------------------------------------------------------------

### Q6. Conditional Probability means:

A. Equal probability

B. Probability given another event

C. Impossible event

D. Random probability

**Answer:** B. Probability given another event

**Explanation:** It depends on another event.

------------------------------------------------------------------------

### Q7. Bayesian Networks help handle:

A. Uncertainty

B. Printing

C. Storage

D. Networking

**Answer:** A. Uncertainty

**Explanation:** They are designed for uncertain environments.

------------------------------------------------------------------------

### Q8. Which is an application of Bayesian Networks?

A. Medical Diagnosis

B. Fraud Detection

C. Recommendation Systems

D. All of the Above

**Answer:** D. All of the Above

**Explanation:** Bayesian Networks are widely used across AI domains.

------------------------------------------------------------------------

### Q9. Which company is known for AI-based medical diagnosis?

A. IBM Watson

B. Spotify

C. Adobe

D. Canva

**Answer:** A. IBM Watson

**Explanation:** IBM Watson applies probabilistic AI in healthcare.

------------------------------------------------------------------------

### Q10. Bayesian Networks mainly perform:

A. Probabilistic reasoning

B. Video editing

C. File compression

D. Image printing

**Answer:** A. Probabilistic reasoning

**Explanation:** They infer probabilities from evidence.

------------------------------------------------------------------------

# One-Line Summary

Bayesian Networks combine probability and graph structures to model
uncertainty and help AI systems make intelligent predictions and
decisions.
