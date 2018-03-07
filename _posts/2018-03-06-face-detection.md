---
layout: post
title: How do they detect faces in pictures?

date: 2018-03-06
categories: artificial-intelligence, deep-learning, machine-learning
tags: 
excerpt_separator: <!--more-->
---

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/singh_harpreet/40619913972/in/album-72157676656040944/" title="face-detection"><img src="https://farm5.staticflickr.com/4747/40619913972_84c7b85a7d.jpg" width="500" height="481" alt="face-detection"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

I was fascinated when Facebook launched the feature where it put a box
around a human head (and a bit creeped out when it started suggesting
the name of the human next to the box). I always wondered how they did
it and filed it under machine-learning magic-ery. Now, I know how they
do it so let me peel back the curtain.
<!--more-->

<p> There are two distinct problem domains in the feature</p>

* Find the human - we will use this blog lifting the curtain behind
the magic.  

* Label the human - this is supervised machine learning and
we will ignore this problem in the blog.  

<p> The "Find the human" problem
is solved through something called "Haar Cascade Classifiers" -
detailed article for brilliant humans 
[link here](https://docs.opencv.org/3.3.0/d7/d8b/tutorial_py_face_detection.html) and the rest follow along
in this blog :-).</p>

The underlying building block is a Classifier but lets drop the
terminology and use airport security as a metaphor to explain the
process.

Think of face detection solution as a airport security problem where a
series of security guards each do a specialised task. The guard at the
airport entrance is responsible to ensure that there is no suspicious
car loitering around the airport. The guard at the security gate is
responsible for letting ones with a valid id and a boarding
ticket. The person behind the scanner is responsible to weed out any
harmful objects in the handbag. The person behind the scanning machine
ensures that no person gets in with a gun. The explosives security
person uses a specialised explosive detector paper and puts in the
machine to find out if hidden explosives are carried by the person
under consideration.

Each of this security guard is a Classifier and classifies a
particular threat. When each is put together in a series, we get a
Cascade of Classifiers. Each building on the work of the other. Each
and everyone of them has to perform their specialised task for a
successful outcome. The successful outcome in this case is that a
person was allowed into the airport lounge and can board his/her
plane. Each of the classifier goes through a great deal of specialised
training for it to perform their task. Makes sense?

So lets apply this metaphor to face detection machine-learning algorithm. In ML, each classifier focusses on a special feature within a picture. The basic classifier tells something as simple as "this is a horizontal edge" or "this is a vertical edge" where edge detection is a feature. This classifier feeds into another one that perhaps says "this is a square" and so on so forth. Eventually, you get to a classifier that tells you "this is a bridge of the nose" or "these are eyes". Each classifier has been fed 100s of thousands of images that are either positive (human in the picture) or negative (no human in the picture) for it to learn to correctly classify the pictures.

So how many such features are there? Turns out a whole lot. For a
typical 24x24 pixel, there are 160k+ features. The Haar in the "Haar
based classifier" is a mathematical function that optimises this
algorithm and reduces the number of features to look out for to about
6k.

Now it turns out that applying this knowledge into our programs is a
lot simpler than the entire training process because opencv.org
provides a python package called opencv to detect these pictures.

I ran a short function to detect humans in about 100 pictures with
humans and ended up with a 100% detection rate - not bad at
all. Running it over 100 dog pictures ended up returning a 89%
accuracy rate. Thus, 11% of dogs were categorised as humans and if you
know me - I think that is fair because some dogs are like humans :-).

My github repo [here](https://github.com/harpreetsingh/udacity-deep-learning-dog-project/blob/master/dog_app.ipynb)
 if you want to see the code, although you can find
it on the Haar based Classifier [link](https://docs.opencv.org/3.3.0/d7/d8b/tutorial_py_face_detection.html)
 as well.