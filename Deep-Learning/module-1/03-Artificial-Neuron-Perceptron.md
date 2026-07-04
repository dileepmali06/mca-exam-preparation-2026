# Module 1 -- Introduction to Deep Learning

# Foundation 03 -- Artificial Neuron (Perceptron)

> **Course:** MCA Semester III -- Deep Learning\
> **Module:** Module 1\
> **Foundation Topic:** Artificial Neuron (Perceptron)

------------------------------------------------------------------------

# Learning Objectives

After completing this topic, you will be able to:

-   Understand why an Artificial Neuron was created.
-   Explain the components of an Artificial Neuron.
-   Understand Inputs, Weights, Bias, Weighted Sum and Activation
    Function.
-   Explain how a Perceptron makes decisions.
-   Relate Artificial Neurons to real-world AI systems.

------------------------------------------------------------------------

# Why Was the Artificial Neuron Created?

Researchers wanted computers to learn like the human brain.

Instead of writing thousands of rules manually, they designed a
mathematical model inspired by biological neurons.

This mathematical model is called an **Artificial Neuron** or
**Perceptron**.

------------------------------------------------------------------------

# Human Brain Inspiration

A biological neuron:

-   Receives signals
-   Processes information
-   Sends signals to other neurons

Similarly, an Artificial Neuron:

-   Receives inputs
-   Performs calculations
-   Produces an output

------------------------------------------------------------------------

# What is an Artificial Neuron?

An Artificial Neuron is the smallest processing unit of a Neural
Network.

Its purpose is to receive information, process it mathematically, and
produce a decision.

------------------------------------------------------------------------

# Components of an Artificial Neuron

``` text
Inputs
   │
   ▼
Weights
   │
   ▼
Weighted Sum
   │
   ▼
Bias
   │
   ▼
Activation Function
   │
   ▼
Output
```

------------------------------------------------------------------------

# 1. Inputs

Inputs are the information given to the neuron.

Examples:

-   Image pixels
-   Text
-   Audio
-   Temperature
-   Student marks

Without inputs, a neuron cannot make any prediction.

------------------------------------------------------------------------

# 2. Weights

Weights represent the importance of each input.

Example:

  Input         Importance
  ------------- ------------
  Location      High
  Area          Medium
  House Color   Low

The neuron learns these weights during training.

------------------------------------------------------------------------

# 3. Weighted Sum

The neuron combines every input according to its importance.

Conceptually:

``` text
(Input × Weight)
+
(Input × Weight)
+
(Input × Weight)

↓

Total Score
```

This total score is called the **Weighted Sum**.

------------------------------------------------------------------------

# 4. Bias

Bias is an additional adjustable value added before making the final
decision.

Think of Bias as a small correction factor that makes the neuron more
flexible.

Example:

A student scores 39 out of 40.

Teacher gives 1 grace mark.

Final score becomes 40.

That extra adjustment is similar to Bias.

------------------------------------------------------------------------

# 5. Activation Function

The Activation Function decides whether the neuron should produce an
output.

``` text
Weighted Sum
      │
      ▼
Activation Function
      │
      ▼
Decision
```

Without an Activation Function, the neuron cannot make meaningful
decisions.

------------------------------------------------------------------------

# Complete Working

``` text
Input Data
      │
      ▼
Apply Weights
      │
      ▼
Calculate Weighted Sum
      │
      ▼
Add Bias
      │
      ▼
Activation Function
      │
      ▼
Final Output
```

------------------------------------------------------------------------

# Real-Life Analogy

Imagine a company hiring a software engineer.

Inputs:

-   Skills
-   Communication
-   Experience
-   Degree

Each factor has different importance (Weight).

Management may also give special consideration (Bias).

Finally, the hiring committee decides:

-   Selected
-   Rejected

The hiring decision is similar to the Activation Function.

------------------------------------------------------------------------

# Software Engineering Analogy

``` text
API Request
      │
      ▼
Validation
      │
      ▼
Business Rules
      │
      ▼
Extra Conditions
      │
      ▼
Success / Failure
```

Mapping:

-   Request → Inputs
-   Importance → Weights
-   Extra Conditions → Bias
-   Final Decision → Activation Function

------------------------------------------------------------------------

# Industry Applications

## Face Recognition

Inputs:

-   Eyes
-   Nose
-   Face Shape

↓

Artificial Neuron

↓

Face Matched

------------------------------------------------------------------------

## Fraud Detection

Inputs:

-   Transaction Amount
-   Device
-   Location
-   Time

↓

Artificial Neuron

↓

Fraud / Genuine

------------------------------------------------------------------------

## Self-Driving Cars

Inputs:

-   Camera
-   Radar
-   Speed
-   Distance

↓

Artificial Neuron

↓

Brake / Turn / Accelerate

------------------------------------------------------------------------

# Visual Architecture

``` text
            Artificial Neuron

x₁   x₂   x₃   x₄
│    │    │    │
▼    ▼    ▼    ▼
w₁   w₂   w₃   w₄
 \    |    |   /
  \   |    |  /
   ▼  ▼    ▼
 Weighted Sum
      │
      ▼
    + Bias
      │
      ▼
Activation Function
      │
      ▼
    Output
```

------------------------------------------------------------------------

# Important Keywords

-   Artificial Neuron
-   Perceptron
-   Inputs
-   Weights
-   Weighted Sum
-   Bias
-   Activation Function
-   Output

------------------------------------------------------------------------

# Quick Revision

-   Inputs provide information.
-   Weights represent importance.
-   Weighted Sum combines all inputs.
-   Bias adjusts the decision boundary.
-   Activation Function decides the final output.

------------------------------------------------------------------------

# Exam Preparation

## 2 Marks

-   Define Artificial Neuron.
-   What is Weight?
-   What is Bias?
-   What is an Activation Function?

## 5 Marks

-   Explain the components of an Artificial Neuron.
-   Explain the working of a Perceptron.

## 10 Marks

Explain the architecture and working of an Artificial Neuron
(Perceptron) with a neat diagram and suitable examples.

------------------------------------------------------------------------

# University Answer Writing Tips

For maximum marks:

1.  Definition
2.  Labelled diagram
3.  Explain every component
4.  Explain the working step-by-step
5.  Add one real-world example
6.  Conclude with applications

------------------------------------------------------------------------

# Summary

An Artificial Neuron (Perceptron) is the basic building block of a
Neural Network.

It receives inputs, assigns importance using weights, calculates a
weighted sum, adjusts it using bias, and finally produces a decision
using an activation function.

Millions of such neurons connected together form modern Deep Learning
models.
