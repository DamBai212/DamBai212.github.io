---
layout: post
title:      "React Props and Sate"
date:       2020-11-23 15:09:34 -0500
permalink:  react_props_and_sate
---


In react, components are responsible for generating HTML. To make HTML generate dynamically we need to pass data to our component so that our component can use variables and serve dynamic HTML.
There are two types of data in react
state (private data available in component only)
props (public data can be passed to component from outside)

![](https://miro.medium.com/max/1000/0*A5-m8E05U2UGUCOl)


**What are props in react?**

Props are basically data that flows from one to another component as a parameter. Props can not be modified in a component.
React Props are like function arguments in JavaScript and attributes in HTML. The component uses this data to generate dynamic HTML elements.
Props are passed to components via HTML attributes.

**What is state in react?**

React components has a built-in state object which is private to a component. State can not be accessed from outside of the class. However, it can be passed as an argument to another component.
Whenever state is changed component calls the render function to render HTML elements.
