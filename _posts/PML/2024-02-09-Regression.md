---
layout: post
title: Regression
category: Practical Machine Learning
mathjax: true
---


Regression  -> continuous numerical value

Classification  -> discrete outputs

typical format of data:
- $X_{i}$ = raw information of the sample
- $Y_{i}$ = class | regression target value

A collection of data sample( X ) = a dataset.

The input and output of regression can be multi-dimensional.

    Is there any example with a single-dimensional input and multi-dimensional output?

    ANS: To predict studnets grade in MATH, COMP and AI based on the time he spended.

# Tradition Types of Regression Models
- Linear Regression
    - Simple Linear Regression
    - Multiple Linear Regression
- Polynomial Regression
- Regularization Methods
    - Ridge Regression (L2 Regularization)
    - Lasso Regression (L1 Regularization)
- Logistic Regression

FOR DNN:\
**Universal Approximation Theorem**: A feedforward neural network with a single hidden layer containing a finite number of neurons can approximate any continuous function

# Simple Linear Regression
Simple linear regression attempts to find the best-fitting straight line through these points.

Y= $ \alpha $ X+$\beta$+$\epsilon$

#### SSR = Sum of squared residuals: 

$ SSR=
  (y_ {i}-(\beta +\alpha x_ {i}))^ {2} $ 


# Multiple Linear Regression
multiple linear regression attempts to find the best-fitting straight plane through data points.

$Y=X\beta+\epsilon$

where $X$ is $n\times(p+1),p$ is the number of feature

$SSR = ||Y-x  \beta   ||_ {2}^ {2}  =  (Y-x\beta )^ {T}  (Y-x  \beta  )$

 $ \beta  =  (X^ {T}X)^ {-1}   X^ {T}  Y$


# Polynomial Regression

$Y=X\beta+\epsilon$

Polynomial regression models the relationship between the independent variable, 𝑥, and the dependent variable (observation), 𝑦, as an 𝑛-th degree polynomial. 

    Higher-degree polynomials can lead to overfitting
    Choose the appropriate degree of polynomials by
        Cross-Validation
        Regularization

# Ridge Regression (L2 Regularization)

$ ||Y-X  \beta $ $ ||_ {2}^ {2}  +  \lambda  ||  \beta  ||_ {2}  ^ {2}  $

$ (X^{T}X+  \lambda  I)  \beta  =  X^ {T}  Y$

$ \beta  =  (X^ {T}X+\lambda I)^ {-1}  X^ {T}  Y$

deal with overfitting\
The model is too complex\
The data samples may not be independent

The L2 penalty encourages smaller, more diffuse coefficient values, leading to a model that is less likely to overfit to the training data.

λ: Tuning parameter that controls the strength of the penalty term.
# Lasso Regression (L1 Regularization)

$ ||Y-X  \beta $ $ ||_ {2}^ {2}  +  \lambda  ||  \beta  ||_ {1}   $

    some factors (e.g., age of owner) are not useful! In many cases, we have designed “over-complicated” models by considering all different factors, which will lead to overfitting.

L1 norm generates sparser solutions!

If sparse solutions can be obtained for 𝜷, we can identify the really useful factors, and make the weights to non-useful factors to zero.

# Logistic Regression
    The Logistic Regression can be used to predict these continuous probability values, while the target follows Bernoulli distribution.

    
further reading: [wiki](https://en.wikipedia.org/wiki/Logistic_regression)