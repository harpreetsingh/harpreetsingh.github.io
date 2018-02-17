---
layout: post
title: Intuitive understanding of a softmax function in a neural network 

date: 2018-02-16
categories: neuralnetwork, deeplearning
tags: deeplearning, neuralnetwork 
excerpt_separator: <!--more-->
---

A softmax function squashes its inputs to be between 0 and 1 and also normalises them so that the sum is equal to 1.

Let's take a problem where we have to classify between three classes. 

Softmax is used to classify for greater than 2 classes for less than 3, use a sigmoid function. So, we need to tell if 
an animal is a duck, a dog or a cat. Our Neural Network linear function looks a picture of an animal and comes back with 
say a score 2 (duck), 1(dog) and -1(cat). The next step is to convert the scores into a probabilities 
whether the picture is a duck, dog or a cat. 

This is where Softmax comes in. The softmax function takes independent scores and comes back with probabilities such
that the sum of these probabilities is equal to 1. Thus, we can classify a picture against these classes relative 
to each other. 

The formula is 
<p>

$$
P(duck) = \frac{e^d}{e^d + e^o + e^c}$$
<p>
where d is duck, o is dOg and c is cat in the formula.

Our end result will look something like: 
<p>
P(duck) = 0.70
<p>
P(dog) = 0.26
<p>
P(cat) = 0.03
<p>
Thus, we have taken a matrix of scores and converted them into probability distributions
$$\begin{bmatrix}
2 & 1 & -1 \\
\end{bmatrix}
$$

Apply <b>softmax</b> to produce

$$\begin{bmatrix}
0.7 \\
0.26 \\
0.03 \\
\end{bmatrix}
$$


Thus, to summarise, a softmax function squashes its inputs called logits to be between 0 and 1 and also normalises them so that the sum is equal to 1.
