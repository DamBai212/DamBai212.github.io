---
layout: post
title:      "Flatiron Final Project"
date:       2020-11-23 20:02:30 +0000
permalink:  flatiron_final_project
---


For my final project at flatiron, I decided to do a simple to-do app with React-redux as the client and ruby on rails as the backend. This was no easy task for me as I’ve spent some time away from coding in React and Ruby(Thanks Covid). Diving in headfirst I came across a few roadblocks connecting my react-app with rails. One noticeable mistake I made was failing to change rails localhost:3000 to localhost:3001. Since my client was running from the same 3000 port. Once passing that hurdle and installing the appropriate gems such as CORS (This gem allows our Rails app to accept Cross-Origin-Resource-Sharing requests (cors) from our React app) and foreman. The initial setup to front-end and back-end was simple.
The next step was creating basic CRUD functionality. So I wanted to 1.create a task, 2. Update that task, 3. Retrieve a task, and finally 4. Delete a task. Initially, I wrote all of my CRUD functions in one component, just to get the app running and some data on the screen. Afterward, I began the process of adding redux to the app while breaking up my code into smaller stateless components. Using redux on this simple app might have seemed like overkill but in actuality, it helped give me a better understanding of state and the natural flow of state props throughout the app.
