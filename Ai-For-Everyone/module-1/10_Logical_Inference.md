# Module 1 -- Introduction to Artificial Intelligence

# Topic 1.2.4 -- Logical Inference

> **Source:** AI for Everyone (Amity University) -- Module 1

------------------------------------------------------------------------

# Learning Objectives

After completing this topic, you should be able to:

-   Define Logical Inference.
-   Explain the need for Logical Inference in AI.
-   Understand Facts, Rules, and the Inference Engine.
-   Differentiate Forward Chaining and Backward Chaining.
-   Explain real-world applications of Logical Inference.

------------------------------------------------------------------------

# Introduction

Knowledge Representation stores knowledge, but Artificial Intelligence
also needs the ability to think and derive new conclusions.

Logical Inference is the reasoning process through which AI applies
logical rules to known facts and generates new knowledge.

------------------------------------------------------------------------

# Why Logical Inference?

AI should not only remember facts but also answer questions and solve
problems.

Example:

Facts: - All birds can fly. - Sparrow is a bird.

Inference:

Sparrow can fly.

------------------------------------------------------------------------

# Definition

> **Logical Inference is the process of deriving new conclusions from
> existing facts, rules, and knowledge using logical reasoning.**

------------------------------------------------------------------------

# Components of Logical Inference

## 1. Facts

Known and verified information.

Example:

-   Sparrow is a bird.
-   Water boils at 100°C.

------------------------------------------------------------------------

## 2. Rules

Logical IF--THEN statements.

Example:

``` text
IF Bird
THEN Can Fly
```

------------------------------------------------------------------------

## 3. Inference Engine

The Inference Engine applies rules to facts and produces conclusions.

Workflow:

``` text
Facts
   │
Rules
   │
Inference Engine
   │
Conclusion
```

------------------------------------------------------------------------

# Rule-Based Reasoning

Example:

``` text
IF Temperature > 40°C
THEN Turn ON AC
```

Another Example:

``` text
IF Balance < ₹100
THEN Send Low Balance Alert
```

------------------------------------------------------------------------

# Forward Chaining

## Definition

Forward Chaining starts from known facts and applies rules until a goal
is reached.

Workflow:

``` text
Facts
   │
Rules
   │
New Facts
   │
Goal
```

Applications:

-   Medical Diagnosis
-   Expert Systems
-   Monitoring Systems

------------------------------------------------------------------------

# Backward Chaining

## Definition

Backward Chaining starts from a goal and works backward to determine
whether supporting facts exist.

Workflow:

``` text
Goal
   │
Required Facts
   │
Knowledge Base
   │
Decision
```

Applications:

-   Troubleshooting
-   Diagnosis
-   Question Answering

------------------------------------------------------------------------

# Forward vs Backward Chaining

  Forward Chaining          Backward Chaining
  ------------------------- --------------------------------
  Starts from facts         Starts from goal
  Data-driven               Goal-driven
  Moves toward conclusion   Moves backward to verify facts

------------------------------------------------------------------------

# Real-World Applications

-   IBM Watson (Medical Diagnosis)
-   Banking Fraud Detection
-   Expert Systems
-   Google Knowledge Systems
-   Smart Assistants
-   Robotics

------------------------------------------------------------------------

# Software Engineering Perspective

Logical Inference is used in:

-   Rule Engines
-   Chatbots
-   Recommendation Systems
-   Fraud Detection Systems
-   Decision Support Systems

Developers implement business rules using logical inference to automate
decisions.

------------------------------------------------------------------------

# Advantages

-   Supports intelligent reasoning
-   Automates decision making
-   Produces logical conclusions
-   Reduces manual effort
-   Improves consistency

------------------------------------------------------------------------

# Quick Revision

-   Logical Inference = Logical reasoning
-   Facts + Rules = Conclusion
-   Inference Engine performs reasoning
-   Forward Chaining = Facts → Goal
-   Backward Chaining = Goal → Facts

------------------------------------------------------------------------

# Important Definitions

## Logical Inference

The process of deriving conclusions using facts and logical rules.

## Fact

Verified information.

## Rule

An IF--THEN statement used for reasoning.

## Inference Engine

The AI component that applies rules to facts and generates conclusions.

------------------------------------------------------------------------

# Important Keywords

-   Logical Inference
-   Reasoning
-   Facts
-   Rules
-   Inference Engine
-   Forward Chaining
-   Backward Chaining
-   Knowledge Base
-   Decision Making
-   Expert System

------------------------------------------------------------------------

# Frequently Asked University Questions

## 2 Marks

1.  Define Logical Inference.
2.  What is an Inference Engine?
3.  What is Forward Chaining?

## 5 Marks

1.  Explain Logical Inference.
2.  Explain Forward and Backward Chaining.

## Long Answer

1.  Explain Logical Inference with suitable examples.
2.  Discuss the role of the Inference Engine in AI.

------------------------------------------------------------------------

# Exam Tips

For maximum marks:

1.  Write the definition.
2.  Draw the inference workflow.
3.  Explain Facts, Rules, and Inference Engine.
4.  Differentiate Forward and Backward Chaining.
5.  Give one real-world example.

------------------------------------------------------------------------

# MCQs

### Q1. Logical Inference is used to:

A. Store Images

B. Derive new conclusions

C. Increase RAM

D. Compress files

**Answer:** B. Derive new conclusions

**Explanation:** Logical Inference applies rules to facts to produce new
conclusions.

------------------------------------------------------------------------

### Q2. Which component performs reasoning?

A. Database

B. Inference Engine

C. Compiler

D. Monitor

**Answer:** B. Inference Engine

**Explanation:** It is responsible for applying rules to facts.

------------------------------------------------------------------------

### Q3. Facts are:

A. Random guesses

B. Verified information

C. Images

D. Programs

**Answer:** B. Verified information

**Explanation:** Facts are known and validated pieces of information.

------------------------------------------------------------------------

### Q4. Rules are commonly written as:

A. HTML Tags

B. IF--THEN Statements

C. SQL Tables

D. CSS Rules

**Answer:** B. IF--THEN Statements

**Explanation:** Rule-based systems commonly use IF--THEN logic.

------------------------------------------------------------------------

### Q5. Forward Chaining starts from:

A. Goal

B. Facts

C. Output

D. Query

**Answer:** B. Facts

**Explanation:** It begins with available facts.

------------------------------------------------------------------------

### Q6. Backward Chaining starts from:

A. Facts

B. Goal

C. Rules

D. Data

**Answer:** B. Goal

**Explanation:** It begins with the goal to verify required facts.

------------------------------------------------------------------------

### Q7. Which AI component applies logical rules?

A. Knowledge Base

B. Inference Engine

C. Database

D. Memory

**Answer:** B. Inference Engine

**Explanation:** It performs logical reasoning.

------------------------------------------------------------------------

### Q8. Which of these uses Logical Inference?

A. Expert Systems

B. Medical Diagnosis

C. Banking Systems

D. All of the Above

**Answer:** D. All of the Above

**Explanation:** Logical Inference is widely used across intelligent
systems.

------------------------------------------------------------------------

### Q9. Forward Chaining is also called:

A. Goal-driven

B. Data-driven

C. Random Search

D. Binary Search

**Answer:** B. Data-driven

**Explanation:** It starts from existing data (facts).

------------------------------------------------------------------------

### Q10. Logical Inference combines:

A. Facts and Rules

B. Images and Videos

C. Programs and Hardware

D. Files and Folders

**Answer:** A. Facts and Rules

**Explanation:** Rules are applied to facts to derive conclusions.

------------------------------------------------------------------------

# One-Line Summary

Logical Inference enables AI systems to derive intelligent conclusions
from facts and rules, making automated reasoning and decision making
possible.
