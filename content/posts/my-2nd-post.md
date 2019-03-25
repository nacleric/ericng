---
title: "OOP in js is weird"
date: 2019-03-21T17:24:10-04:00
draft: true
---

I'm pretty sure most people can relate, the way I tend to learn a new language is to compare certain features to a language that I'm already familiar with. In my case, it was python's dictionary.

Javascript has a prototype inheritance model, which I don't quite understand if I'm being honest.
Basically I tried to make a key-value pair writing it the same way as I would declare a dictionary in python. I still got my intended effect but it's technically a javascript object with a value being referenced to it. I've always heard people talk about how janky javascript was but this was my first real moment seeing some of javascripts inconsistencies.

{{< highlight javascript "linenos=table,linenostart=1" >}}

let obj = {
firstName: "bob",
"lastName": "ross"
}

> obj['firstName'] 
//'bob'
> obj.lastName
//'ross'

{{< / highlight >}}

Obviously no one would ever do something like this. But it just leaves a bad impression knowing javascript goes out of its way to let things compile, to the point where you can make a method call for something declared as a string.

I kind of get it in a way. This syntax leniancy can be seen in HTML and CSS, but the worse case scenario for these markup languages is the DOM just not being rendered, but the opposite can't be said for javascript. Not catching these small JS syntax errors during compile time should seem like something thats mandatory in 2019. The web is way more than just text being rendered on a screen and having these errors passed silently is a major problem.