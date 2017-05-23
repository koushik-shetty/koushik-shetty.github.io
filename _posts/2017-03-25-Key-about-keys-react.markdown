---
layout: post
title:  "Key about Key - React[WIP]"
date:   2017-05-23 06:46:34 -0400
categories: dev
tags: [React, key, javascript]
---
React components can have a special `prop` called `key`. This prop is important when a __array__ of components is rendered, in a loop. i.e they are used when you turn an array of your data to a list of react elements.

This prop serves one important reason: __Caching__  
`Key` provides the identity to a component within the list and react uses this identity to cache the component while rendering. if the key is not present then it renders the DOM that the component represents else uses the already rendered component.

#### __Why is `key` important?__  
As mentioned above `key` helps in caching. This is not usable prop for the component itself, meaning that we cannot and should not access it. 

{% highlight javascript %}
<Item key={i} data={data}/>
{% endhighlight %}
