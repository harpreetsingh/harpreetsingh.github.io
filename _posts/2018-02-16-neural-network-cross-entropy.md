---
layout: post
title: Understanding cross entropy in a neural network 

date: 2018-02-16
categories: neuralnetwork, deeplearning
tags: deeplearning, neuralnetwork 
excerpt_separator: <!--more-->
---

Let's say that there are a bunch of events and a bunch of probabilities, cross entropy predicts how likely are those
events likely to happen based on the probabilities.

A high cross entropy means that an event is unlikely to happen while a low event indicates that the event will happen. 

In a neural network (NN), an error function is used to classify data into appropriate classifications. So in well 
performing NN the goal is to minimise the output of the error function. Another way to look at this minimization is 
that we should be increasing the probabilities that these points are classified right. Thus, we are aiming to get 
the probabilities of the events to get higher.

Let's take an example - where we have 3 doors and if we open the door, we are likely to either find a duck, dog or a cat 
behind each door. These events are independent to each other, thus all 3 doors can have a dog behind them.

Let's say the most likely probability is to find the following behind each doors:
<p>
Door 1 = P(duck) = 0.70
<p>
Door 2 = P(dog) = 0.80
<p>
Door 3 = P(cat) = 0.97
<p>
   
Thus, the likely hood of finding a duck, a dog and a cat is
$$
0.7*0.8*0.97 = 0.6
$$   

Since multiplication of various events with numbers less that 1 could be very small, we typically use the logarithm 
function to add them up and that is the formula for Cross entropy

$$Cross entropy = -log(0.7) - log(0.8) - log(0.9)$$
 
$$Cross entropy = -(-0.35566) - (-0.2231) - (-0.1053)$$

$$Cross entropy = 0.685$$

This low cross entropy number indicates that the likelihood that these events (of a duck, dog, cat ) showing up behind 
the doors is high.

To implement this in tensorflow, you'd do the following:

```python
softmax_data = [0.7, 0.2, 0.1]
one_hot_data = [1.0, 0.0, 0.0]

softmax = tf.placeholder(tf.float32)
one_hot = tf.placeholder(tf.float32)

cross_entropy = -tf.reduce_sum(tf.multiply(one_hot, tf.log(softmax)))
```
