---
layout: post
title: Understanding neural networks - a dog lovers primer
date: 2017-03-03
categories: deep-learning
tags: deep-learning
excerpt_separator: <!--more-->
---

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/singh_harpreet/20774526803/in/album-72157656253958874/" title="Untitled"><img src="https://c1.staticflickr.com/1/683/20774526803_3215449907.jpg" width="500" height="375" alt="Untitled"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>


Let’s look at a problem: I am a dog lover and I subscribe to Instagram where I get a stream of images of toasters, birds, cats and dogs. While these images are exciting (who doesn’t like toasters :-)), what I want to do, is automatically save images of dogs to an account on the cloud. The question is, what kind of program do I need to write that tags all dog images to feed my cloud database of awesome-dog-images.

<!--more-->

**A neural network to the rescue!**

A neural network is a decision engine. Its job is to look at in-coming data and make a decision about the data. Typically, a neural network uses logistic regression to make these decisions. I covered regressions here - logistic regression classifies data into a yes/no class of answers.

# Building a neural network is like training a dog.

* You train the dog to obey a command
* Analyse if the dog is behaving right in all field conditions and
* Provide the appropriate feedback to fix any problems

# “Sit boy” - Training the neural network

To get something useful from a neural network - you need to train it. To do this you take the existing set and split into the data you train with and the data you test against.

# Training the data

In the data here, I have two regression lines that neatly separates the images. In neural network parlance, each quadrant is a decision node that outputs yes/no if it identifies the data right. Each node is called a perceptron or neuron. Each one looks at input data and decides how to categorise that data. In the example above, the input either passes a threshold for dogs, cats, birds and toasters and each neuron answers a yes or no.

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/singh_harpreet/33117754681/in/album-72157676656040944/" title="neural-network-dog-classifier"><img src="https://c1.staticflickr.com/4/3706/33117754681_a905397d50.jpg" width="321" height="299" alt="neural-network-dog-classifier"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>


You write a function called an **activation** function to make the decision. Typically, an activation function uses a **heaviside** activation function i.e. the function returns false if the number is < 0 and returns true if a number is greater than 0. Each function takes a weight (w) that determines how important the function is. **This is really important - the weights determine if a network is going to be successful**. For example as I am looking for a dog, the activation function for dogs will have a heavier value than for a cat. If on the other hand, I was looking to classify toasters, the weight for toaster would be greater than that for mammals and birds. The output of these functions will go through an aggregator function that determines the final output. The activation function is the key as it is this function that determines what the answer is going to be.

The network above has only **forward propagation** as in each neuron makes a decision and pushes the answer forward. Thus, once you have trained the network and the network makes errors, it will continue making the error forever. What makes this picture interesting and useful is if you can find the error between the right value and the error and feed it back to the network. This is called **back propagation**.

# Is the dog doing the right thing: Analysing the output

Did the dog do the right thing? A dog sleeping on the sofa while I gave it a sit command is an epic fail. Isn't it?

In neural networks, you take your test data and feed it through the network to see the output. The good thing with the test data is that we already know the answer. You compare the result from the network to the test data and determine the delta. The delta tells you how off you are from the right answer. We will get into more details in another blog perhaps.

# Provide feedback to the dog to fix issues: Provide feedback to the network

Once you have the delta from the network, you feed it back into the network. This process is called back-propagation. The way to think about back-propagation is that it is a _mirror of the neural network_, where instead of starting from the inputs you start with the error instead. You start with the derived answer and the actual answer, calculate the delta for the error and start updating the weights on the way back. You do so for each record in the data set. You typically use gradient descent to find the right weights on the way back.

To sum up - weights are what helps determine the right answer but you don’t get the right weights when you only move in one direction, so you find the error and fix the weights back and voila you have a neural network that has learnt.

Congratulations! You have now successfully trained your dog - welcome to a great life ahead.
<a data-flickr-embed="true"  href="https://www.flickr.com/photos/singh_harpreet/21208234279/in/album-72157656253958874/" title="Untitled"><img src="https://c1.staticflickr.com/6/5828/21208234279_0632463b60.jpg" width="375" height="500" alt="Untitled"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>
