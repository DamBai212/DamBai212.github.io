---
layout: post
title:      "Getting Familiar with CORS"
date:       2019-04-13 16:20:07 -0400
permalink:  getting_familiar_with_cors
---


   CORS might be an unfamiliar concept to some students at Flatiron School mainly because the labs have built-in TDDs with set conditions. This may prevent noticeable CORS errors from happening mainly due to the fact that the data we fetch is open source. CORS which is short for Cross-Origin Resource Sharing was created for allowing users to make a secure request while blocking sketchy requests made by rogue JS. So basically CORS is used for secure cross-site HTTP requests. Below is an example of these requests working under the hood.

![](https://mdn.mozillademos.org/files/14295/CORS_principle.png)

Simply put CORS is a mechanism that prevents hackers rogue JS from making AJAX calls to confidential information that would end up in the wrong hands. Creating a secure environment for the user and the site being requested. It's to be noted that if you do come across a CORS error, the problem might actually be caused by the lack of headers on the client-side. 

The solution  I found most practical on handling this issue was by using a CORS-as-a-service solution such as https://cors-anywhere.herokuapp.com/ , this URL adds headers to the request under the hood. I’ve added a link on more documentation of CORS. [Link](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)
