# Module 1 -- Introduction to Artificial Intelligence

# Topic 1.1.6 -- Adversarial Search

> **Source:** AI for Everyone (Amity University) -- Module 1

------------------------------------------------------------------------

# Learning Objectives

After completing this topic, you should be able to:

-   Define Adversarial Search.
-   Understand why Adversarial Search is required.
-   Explain the concept of a Game Tree.
-   Describe the Minimax Algorithm.
-   Explain Alpha-Beta Pruning.
-   Identify real-world applications of Adversarial Search.

------------------------------------------------------------------------

# 1. Introduction

Unlike normal search problems, many Artificial Intelligence applications
involve competition between two intelligent agents.

In such situations, one player's success depends on the opponent's
actions.

This type of search is known as **Adversarial Search**.

Examples include:

-   Chess
-   Tic-Tac-Toe
-   Checkers
-   Poker
-   Strategy Games

------------------------------------------------------------------------

# 2. Definition

> **Adversarial Search is a search technique used in competitive
> environments where an intelligent agent selects the best possible
> action while considering the possible actions of an opponent.**

------------------------------------------------------------------------

# 3. Normal Search vs Adversarial Search

  Normal Search                Adversarial Search
  ---------------------------- --------------------------------
  No Opponent                  Intelligent Opponent
  Goal is to find a solution   Goal is to defeat the opponent
  Examples: Google Maps, GPS   Examples: Chess, Tic-Tac-Toe

------------------------------------------------------------------------

# 4. Game Tree

A Game Tree is a tree structure representing every possible move in a
game.

Example:

``` text
            Start
           /     \
      Move A    Move B
      /   \      /   \
    A1    A2   B1    B2
```

Each node represents a game state.

Each branch represents a possible move.

------------------------------------------------------------------------

# 5. Minimax Algorithm

## Definition

The Minimax Algorithm is a decision-making algorithm used in
game-playing AI.

The AI tries to:

-   Maximize its own score.
-   Minimize the opponent's score.

Hence the name **Mini + Max = Minimax**.

------------------------------------------------------------------------

## Working

    Current State
          │
    Possible Moves
          │
    Opponent Responses
          │
    Evaluate Outcomes
          │
    Choose Best Move

------------------------------------------------------------------------

## Characteristics

-   Decision-making algorithm
-   Used in two-player games
-   Assumes an intelligent opponent
-   Explores future possibilities

------------------------------------------------------------------------

# 6. Alpha-Beta Pruning

Alpha-Beta Pruning is an optimization technique used with the Minimax
Algorithm.

Instead of evaluating every possible move, unnecessary branches are
skipped.

Advantages:

-   Faster execution
-   Reduced computation
-   Same final decision

------------------------------------------------------------------------

# 7. AI Workflow

``` text
Current Game State
        │
Possible Moves
        │
Game Tree
        │
Minimax Evaluation
        │
Alpha-Beta Pruning
        │
Best Move
```

------------------------------------------------------------------------

# 8. Real-World Applications

-   Chess AI
-   Tic-Tac-Toe AI
-   Checkers
-   Military Simulations
-   Strategy Games
-   Robotics Competitions

------------------------------------------------------------------------

# 9. Software Engineering Perspective

Adversarial Search concepts are commonly used in:

-   Game Development
-   AI Game Bots
-   Multiplayer Games
-   Strategy Simulations

Developers implement Minimax and Alpha-Beta Pruning to build intelligent
game-playing agents.

------------------------------------------------------------------------

# Quick Revision

-   Adversarial Search = Competitive Search
-   Opponent = Adversary
-   Game Tree = Possible game states
-   Minimax = Best move selection
-   Alpha-Beta Pruning = Skip unnecessary branches

------------------------------------------------------------------------

# Important Definitions

## Adversarial Search

A search technique used in competitive environments where an AI agent
considers the opponent's actions before making decisions.

## Game Tree

A tree representation of all possible game states.

## Minimax Algorithm

A decision-making algorithm that maximizes the AI's score while
minimizing the opponent's score.

## Alpha-Beta Pruning

An optimization technique that reduces unnecessary game tree evaluation
without affecting the final decision.

------------------------------------------------------------------------

# Important Keywords

-   Adversarial Search
-   Game Tree
-   Minimax
-   Alpha-Beta Pruning
-   Game State
-   Opponent
-   Decision Making
-   Strategy
-   Competitive AI
-   Game Playing

------------------------------------------------------------------------

# Frequently Asked University Questions

## 2 Marks

1.  Define Adversarial Search.
2.  What is a Game Tree?
3.  What is the Minimax Algorithm?

## 5 Marks

1.  Explain Adversarial Search.
2.  Explain the Minimax Algorithm.
3.  Explain Alpha-Beta Pruning.

## Long Answer

1.  Explain Adversarial Search with suitable examples.
2.  Explain Minimax Algorithm using a Game Tree.
3.  Differentiate Normal Search and Adversarial Search.

------------------------------------------------------------------------

# MCQs

### 1. Adversarial Search is mainly used in:

A. Databases

**B. Game Playing AI ✅**

C. Image Editing

D. Networking

------------------------------------------------------------------------

### 2. An opponent in Adversarial Search is called:

A. Client

**B. Adversary ✅**

C. Server

D. Host

------------------------------------------------------------------------

### 3. Which algorithm is most commonly associated with Adversarial Search?

A. Binary Search

**B. Minimax ✅**

C. Bubble Sort

D. Linear Search

------------------------------------------------------------------------

### 4. A Game Tree represents:

A. Database Tables

**B. Possible Game States ✅**

C. Computer Network

D. Images

------------------------------------------------------------------------

### 5. Minimax attempts to:

A. Maximize the opponent's score

**B. Maximize AI's score while minimizing the opponent's score ✅**

C. Ignore the opponent

D. End the game immediately

------------------------------------------------------------------------

### 6. Alpha-Beta Pruning helps by:

A. Increasing memory usage

**B. Eliminating unnecessary branches ✅**

C. Creating new nodes

D. Sorting data

------------------------------------------------------------------------

### 7. Which game commonly uses Adversarial Search?

A. Calculator

**B. Chess ✅**

C. Word Processor

D. Paint

------------------------------------------------------------------------

### 8. Deep Blue is associated with:

A. Google

**B. IBM ✅**

C. OpenAI

D. NVIDIA

------------------------------------------------------------------------

### 9. Minimax is primarily used for:

A. File Compression

**B. Decision Making in Games ✅**

C. Database Design

D. Operating Systems

------------------------------------------------------------------------

### 10. Which statement is correct?

A. Adversarial Search ignores opponents.

B. Alpha-Beta Pruning changes the final decision.

**C. Adversarial Search evaluates both the player's and opponent's
moves. ✅**

D. Minimax is used only in databases.

------------------------------------------------------------------------

# One-Line Summary

Adversarial Search enables AI to make intelligent decisions in
competitive environments by analyzing future moves, evaluating game
states, and selecting the optimal strategy using algorithms such as
Minimax and Alpha-Beta Pruning.
