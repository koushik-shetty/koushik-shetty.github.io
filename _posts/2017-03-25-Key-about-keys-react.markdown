---
layout: post
title:  "Key about Key - React[WIP]"
date:   2017-05-23 06:46:34 -0400
categories: dev
tags: [React, key, javascript]
---
React components can have a special `prop` called `key`. This prop is important when a __array__ of components is rendered, in a loop. i.e they are used when you turn an array of your data to a list of react elements.

This prop serves one important purpose: __Caching__  
`Key` provides the identity to a component within the list and react uses this identity to cache the component while rendering.

#### __Why is `key` important?__  
As mentioned above `key` helps in caching. This is not usable prop for the component itself, meaning that we cannot access it.
When react tries to render this array, it checks if the component with the key is present in its instance cache or not. if it is not present then it creates the instance of the component and renders the DOM that it represents(create lifecycle) else it uses the already created instance and renders the DOM with the updated `props`(and`state`) (update lifecycle). This is a lot of performace boost which will avoid uneccessary painting, going hand in hand with reacts VDOM technology.


{% highlight html %}
<Item key={i} data={data}/>
{% endhighlight %}
