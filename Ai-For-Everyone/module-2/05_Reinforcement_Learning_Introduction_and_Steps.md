# Module 2 -- Artificial Intelligence with Python

# Lesson 5

## 2.3.1 -- Introduction to Reinforcement Learning

## 2.3.2 -- Formal Definition of Reinforcement Learning

## 2.3.3 -- Steps of Reinforcement Learning

> **Source:** AI for Everyone (MCA Semester III)

------------------------------------------------------------------------

# Learning Objectives

After completing this lesson, you should be able to:

-   Define Reinforcement Learning (RL).
-   Explain why RL is required.
-   Understand Agent, Environment, Action, and Reward.
-   Describe the Reinforcement Learning cycle.
-   Explain the steps of Reinforcement Learning.
-   Identify real-world applications of RL.

------------------------------------------------------------------------

# Introduction

Reinforcement Learning (RL) is a branch of Machine Learning in which an
intelligent agent learns by interacting with its environment. The agent
performs actions, receives rewards or penalties, and gradually improves
its decision-making ability.

------------------------------------------------------------------------

# Why Reinforcement Learning?

Some problems do not have correct answers available beforehand.

Examples:

-   Self-driving cars
-   Game playing
-   Robotics
-   Drone navigation

Instead of learning from labeled data, RL learns from experience.

------------------------------------------------------------------------

# Definition

> **Reinforcement Learning is a type of Machine Learning in which an
> agent learns by interacting with the environment and receives rewards
> or penalties for its actions.**

------------------------------------------------------------------------

# Core Components

## 1. Agent

The decision-making entity.

Examples:

-   Robot
-   Self-driving car
-   Chess player AI

------------------------------------------------------------------------

## 2. Environment

The world in which the agent operates.

Examples:

-   Road
-   Video Game
-   Chess Board

------------------------------------------------------------------------

## 3. Action

An operation performed by the agent.

Examples:

-   Move Left
-   Move Right
-   Brake
-   Accelerate

------------------------------------------------------------------------

## 4. Reward

Feedback received after an action.

-   Positive Reward → Good action
-   Negative Reward (Penalty) → Bad action

------------------------------------------------------------------------

# Reinforcement Learning Workflow

``` text
Agent
   │
Take Action
   │
Environment
   │
Reward / Penalty
   │
Learning
   │
Better Action
```

------------------------------------------------------------------------

# Steps of Reinforcement Learning

1.  Observe the environment.
2.  Choose an action.
3.  Perform the action.
4.  Receive reward or penalty.
5.  Learn from feedback.
6.  Repeat until performance improves.

------------------------------------------------------------------------

# Reinforcement Learning Cycle

``` text
Observe
   │
Choose Action
   │
Perform Action
   │
Receive Reward
   │
Learn
   │
Repeat
```

------------------------------------------------------------------------

# Reinforcement Learning vs Supervised Learning

  Supervised Learning         Reinforcement Learning
  --------------------------- ------------------------------
  Uses labeled data           Learns through rewards
  Correct answers available   No correct answers initially
  Learns from examples        Learns from interaction

------------------------------------------------------------------------

# Real-World Applications

-   Self-driving Cars
-   Robotics
-   AlphaGo
-   Warehouse Automation
-   Drone Navigation
-   Advertisement Optimization
-   Stock Trading

------------------------------------------------------------------------

# Software Engineering Perspective

Developers integrate RL in:

-   Autonomous robots
-   Route optimization
-   Intelligent game AI
-   Recommendation optimization
-   Resource allocation systems

Example:

``` text
User Request
     │
RL Agent
     │
Best Decision
     │
User Response
```

------------------------------------------------------------------------

# Advantages

-   Learns through experience
-   Suitable for sequential decision making
-   Adapts to changing environments
-   Improves automatically over time

------------------------------------------------------------------------

# Limitations

-   Requires many training iterations
-   Can be computationally expensive
-   Reward design is challenging

------------------------------------------------------------------------

# Quick Revision

-   RL = Learning through rewards
-   Agent = Decision maker
-   Environment = Surroundings
-   Action = Task performed
-   Reward = Feedback
-   Goal = Maximize cumulative rewards

------------------------------------------------------------------------

# Important Definitions

## Reinforcement Learning

A Machine Learning technique where an agent learns from rewards and
penalties.

## Agent

The entity that takes actions.

## Environment

The external world where the agent acts.

## Action

A decision taken by the agent.

## Reward

Feedback indicating whether an action is good or bad.

------------------------------------------------------------------------

# Important Keywords

-   Reinforcement Learning
-   Agent
-   Environment
-   Action
-   Reward
-   Penalty
-   Learning
-   Decision Making
-   Optimization
-   Sequential Learning

------------------------------------------------------------------------

# Frequently Asked University Questions

## 2 Marks

1.  Define Reinforcement Learning.
2.  What is an Agent?
3.  What is a Reward?

## 5 Marks

1.  Explain Reinforcement Learning.
2.  Explain the components of Reinforcement Learning.

## Long Answer

1.  Explain Reinforcement Learning with a diagram.
2.  Explain the steps of Reinforcement Learning with examples.
3.  Differentiate Reinforcement Learning and Supervised Learning.

------------------------------------------------------------------------

# Exam Tips

To score maximum marks:

1.  Write the definition.
2.  Draw the RL workflow.
3.  Explain Agent, Environment, Action, and Reward.
4.  Explain the RL steps.
5.  Give at least two real-world applications.

------------------------------------------------------------------------

# MCQs

### Q1. Reinforcement Learning learns through:

A. Labeled Data

B. Reward and Penalty

C. Sorting

D. Databases

**Answer:** B. Reward and Penalty

**Explanation:** RL improves using feedback.

------------------------------------------------------------------------

### Q2. The decision maker in RL is:

A. Environment

B. Agent

C. Dataset

D. Model

**Answer:** B. Agent

**Explanation:** The agent selects actions.

------------------------------------------------------------------------

### Q3. The world in which the agent operates is called:

A. Environment

B. Feature

C. Label

D. Dataset

**Answer:** A. Environment

**Explanation:** The environment provides situations and feedback.

------------------------------------------------------------------------

### Q4. Feedback after an action is called:

A. Reward

B. Feature

C. Dataset

D. Prediction

**Answer:** A. Reward

**Explanation:** Rewards or penalties guide learning.

------------------------------------------------------------------------

### Q5. RL is mainly suitable for:

A. Sequential decision making

B. File compression

C. HTML design

D. Text editing

**Answer:** A. Sequential decision making

**Explanation:** RL excels in decision-making tasks.

------------------------------------------------------------------------

### Q6. AlphaGo is an example of:

A. Reinforcement Learning

B. Bubble Sort

C. SQL

D. CSS

**Answer:** A. Reinforcement Learning

**Explanation:** AlphaGo learned game strategies using RL techniques.

------------------------------------------------------------------------

### Q7. Which company developed AlphaGo?

A. Google DeepMind

B. Amazon

C. OpenAI

D. Meta

**Answer:** A. Google DeepMind

**Explanation:** DeepMind created AlphaGo.

------------------------------------------------------------------------

### Q8. Which component gives feedback?

A. Reward

B. Action

C. Dataset

D. Feature

**Answer:** A. Reward

**Explanation:** Reward tells the agent how good its action was.

------------------------------------------------------------------------

### Q9. The main goal of RL is to:

A. Maximize cumulative rewards

B. Increase RAM

C. Compress files

D. Build websites

**Answer:** A. Maximize cumulative rewards

**Explanation:** RL seeks the highest long-term reward.

------------------------------------------------------------------------

### Q10. Which is NOT a core RL component?

A. Agent

B. Environment

C. Compiler

D. Reward

**Answer:** C. Compiler

**Explanation:** A compiler is unrelated to RL.

------------------------------------------------------------------------

# One-Line Summary

Reinforcement Learning enables intelligent agents to learn optimal
decisions by interacting with the environment and maximizing rewards
over time.
