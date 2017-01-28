---
layout: post
title: Udacity Deeplearning course setup for Anaconda
date: 2017-01-28
categories: deeplearning
tags: deeplearning
excerpt_separator: <!--more-->
---
<a data-flickr-embed="true"  href="https://www.flickr.com/photos/singh_harpreet/31869065812/in/album-72157678564264675/" title="Untitled"><img src="https://c1.staticflickr.com/1/714/31869065812_1f0d5dd549_z.jpg" width="640" height="427" alt="Untitled"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

This blog sets up the core software requirements for the Udacity
[deeplearning
course](https://www.udacity.com/course/deep-learning-nanodegree-foundation--nd101) to get you started quickly.

<!--more-->
I have just signed up for the deeplearning course and am
fairly excited about it. The course heavily depends on Python - I used
Python about 18 years back and have been a java guy since. The course
requires you to setup Python 3.5, a number of data packages as part of
Anaconda (a data science platform for analytics).

Rather than struggle with requirements on my Mac again and again, I
have setup a docker image that is up-to date with all the core
requirements for this coursework. Here is what you need to do get the
docker image and run jupyter (which is wiki system for data analysis).

       docker run -i -t -p 8888:8888 hsingh/anaconda-deeplearning
       cd /home/jupyter
       jupyter notebook --ip='*' --port=8888

To bring up the Jupyter notebook, go to your browser on the host machine and enter
   
	http://localhost:8888