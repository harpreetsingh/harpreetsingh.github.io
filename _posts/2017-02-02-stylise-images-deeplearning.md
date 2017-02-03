---
layout: post
title: Building your own prisma with deeplearning
date: 2017-02-02
categories: deeplearning
tags: deeplearning
excerpt_separator: <!--more-->
---

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/singh_harpreet/32678079545/in/album-72157678354798510/" title="Untitled"><img src="https://c1.staticflickr.com/1/772/32678079545_d3c3ebd07a_z.jpg" width="640" height="428" alt="Untitled"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

There are some things that completely blow your mind. Applying artist
specific styles to images is one of them. Completely sci-fiction -
although the Prisma filter has made this accessible.

<!--more-->

In the [last
blog](http://harpreetsingh.github.io/blog/2017/01/28/deeplearning-udacity-setup), I set up the core software requirements for the Udacity [deeplearning
course](https://www.udacity.com/course/deep-learning-nanodegree-foundation--nd101). This blog uses the setup to transfer the styles of 3 famous paintings and
apply it to images.

It takes ages for an artist to come to a signature style. It takes
longer for another to mimic the style and I cannot fathom if a mimic
can apply the style to different images. Deep learning does it with
panache. Impressive! I am a convert.

I used the project called [fast-style-transfer](https://github.com/lengstrom/fast-style-transfer) and ran the
following command on an image to produce an output.

~~~
# creating a sandbox environment for python
conda create -n style-transfer python=3.5
source activate style-transfer
conda install -c conda-forge tensorflow=0.11.0
conda install scipy pillow

# doing style transfer
python evaluate.py --checkpoint ./rain-princess.ckpt --in-path <path_to_input_file> --out-path ./output_image.jpg

~~~

# Pictures to be stylised
<a data-flickr-embed="true"  href="https://www.flickr.com/photos/singh_harpreet/32678078365/in/album-72157678354798510/" title="Untitled"><img src="https://c1.staticflickr.com/1/514/32678078365_35f9c27176_n.jpg" width="320" height="214" alt="Untitled"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/singh_harpreet/32678079175/in/album-72157678354798510/" title="Untitled"><img src="https://c1.staticflickr.com/1/596/32678079175_c7dc015382_n.jpg" width="320" height="214" alt="Untitled"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

# The original artwork:

## The Wave by Kanagawa
<a data-flickr-embed="true"  href="https://www.flickr.com/photos/singh_harpreet/32678082665/in/album-72157678354798510/" title="Untitled"><img src="https://c1.staticflickr.com/1/301/32678082665_b9a5241213_n.jpg" width="320" height="178" alt="Untitled"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

## Scream by Edward Munch
<a data-flickr-embed="true"  href="https://www.flickr.com/photos/singh_harpreet/32678081765/in/album-72157678354798510/" title="Untitled"><img src="https://c1.staticflickr.com/1/419/32678081765_99f1bb9ff4_n.jpg" width="276" height="320" alt="Untitled"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

## Rain Princess by Leonid Affremov
<a data-flickr-embed="true"  href="https://www.flickr.com/photos/singh_harpreet/32678081045/in/album-72157678354798510/" title="Untitled"><img src="https://c1.staticflickr.com/1/338/32678081045_091c475a32_n.jpg" width="320" height="319" alt="Untitled"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

# The modified images
<a data-flickr-embed="true"  href="https://www.flickr.com/photos/singh_harpreet/32678079725/in/album-72157678354798510/" title="Untitled"><img src="https://c1.staticflickr.com/1/780/32678079725_b6fac8c5ed_n.jpg" width="320" height="214" alt="Untitled"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/singh_harpreet/32678079545/in/album-72157678354798510/" title="Untitled"><img src="https://c1.staticflickr.com/1/772/32678079545_d3c3ebd07a_n.jpg" width="320" height="214" alt="Untitled"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/singh_harpreet/32678079225/in/album-72157678354798510/" title="Untitled"><img src="https://c1.staticflickr.com/1/675/32678079225_2a21acce9e_n.jpg" width="320" height="214" alt="Untitled"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/singh_harpreet/32678078625/in/album-72157678354798510/" title="Untitled"><img src="https://c1.staticflickr.com/1/634/32678078625_c04eb3f9da_n.jpg" width="320" height="214" alt="Untitled"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/singh_harpreet/32678078425/in/album-72157678354798510/" title="Untitled"><img src="https://c1.staticflickr.com/1/270/32678078425_595628d1f9_n.jpg" width="320" height="214" alt="Untitled"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>