---
layout: post
title: React Native - Implement scrolling
date: 2017-09-30
categories: programming, ios, react-native
tags: React, React-Native, ios, iphone  
excerpt_separator: <!--more-->
---

Building a scrollable component in react native is fairly easy but comes with a gotcha.
# Use ScrollView instead of View
Simple enough. I had a View component that looked like the following:
```javascript
<View>
  { this.renderAlbums() }
</View>
```

This was replaced with
```javascript
<ScrollView>
  { this.renderAlbums() }
</ScrollView>
```

# gotcha
The gotcha was that I had to change the top level application code to bring in a style with a flex of 1. I don't quite know why!

```javascript
const App = () => (
    <View style={{ flex: 1 }} >
        <Header headerText={'Albums'} />
        <AlbumList />
    </View>
);
```
