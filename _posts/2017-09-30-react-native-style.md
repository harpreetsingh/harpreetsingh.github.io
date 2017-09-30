---
layout: post
title: React Native Component Styling
date: 2017-09-30
categories: programming, ios, react-native
tags: React, React-Native, ios, iphone  
excerpt_separator: <!--more-->
---

Unlike web apps React Native doesn’t have universal styling that is specified via a css. React solves it by asking developers to marry the styling within the component file. As a developer, I found this very convenient to work with - I knew exactly what styling I had to bring into my component. That said, I would expect this to be a challenge working with a designer requiring a constant back and forth. Here is an example of a component that I put together.

# Pre-Styling

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/singh_harpreet/36703194224/in/album-72157676656040944/" title="React-Native-Component-Style-1"><img src="https://farm5.staticflickr.com/4404/36703194224_6197f1c126.jpg" width="230" height="500" alt="React-Native-Component-Style-1"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

# Post-Styling

<a data-flickr-embed="true"  href="https://www.flickr.com/photos/singh_harpreet/36703185534/in/album-72157676656040944/" title="React-Native-Component-Style-2"><img src="https://farm5.staticflickr.com/4396/36703185534_57b5ce9448.jpg" width="234" height="500" alt="React-Native-Component-Style-2"></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

# Code

```javascript
import React from 'react';
import { View } from 'react-native';

const Card = (props) => {
    return (
        <View style={styles.containerStyle}>
            {props.children}
        </View>
    );
};

const styles = {
    containerStyle: {
        borderWidth: 1,
        borderRadius: 2,
        borderColor: '#ddd',
        borderBottomWidth: 0,
        shadowColor: '#000',
        shadowOffset: { width: 0, height: 2 },
        shadowOpacity: 0.1,
        shadowRadius: 2,
        elevation: 1,
        marginLeft: 5,
        marginRight: 5,
        marginTop: 10

    }
};

export default Card;
```
