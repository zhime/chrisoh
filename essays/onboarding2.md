---
layout: essay
type: essay
title: "Onboarding 2"
date: 2018-08-30
labels:
  - Engineering
---
This onboarding task really immersed me into TechFolioDesigner. Although the enhancements were simple, they required me to understand the file structure and implementations for many parts of the program, parts that I otherwise not have looked at. 

For the first enhancement, I made the background of the splash screen lightgrey, a CSS predefined colors. For my first attempt, I created a class for the div tag that rendered the jsx, however the react component seemed to have overrided the styles in its div tag. So I created a CSS class for the body tag that holds the splash page to change the background color. I had to add the CSS splash class in style.css and modify SplashPage.html to use the background color changing class.

For the second enhancement, I had to add a "Last Modified" time stamp that informs the user when the last change took place, regarding the table or text in the command log. I attempted to do this by making a component that shows the last modified time, the time being the first 10 characters of the status property from redux. But I later realized that my implementation of the feature only informs the user when the last "Check local directory status" is clicked, rather than all of the changes in TechFolio designer. And I didn't use MomentJS, which would've done the job easier. I will definitely update this enhancement. 

Adding a menu item sounded simple in theory, but I encountered an issue where my current time window would come up when the program starts (before the "Get Current Time" option is even clicked), and when "Get Current Time" is clicked, despite being enabled, wouldn't open the window. I will fix this issue.

The simple validation to the Set Github Repo name was a very easy fix. In ConfigSubMenu.js, I added an if statement to check if the last 10 characters of the entered repo name are exactly ".github.io". 

Allowing four networks in the simple bio editor was also simple, but tedious. I manually entered a fourth copy of the network and all of its properties in SimpleBioEditorTabNetwork.jsx. 

The last simple validation, and last enhancement for the onboarding task was also simple, but required some knowledge of regex. Like the github repo validation, this enhancement simply required an if statement in the saveFile function. I used notifier (node-notifier) because the file was saved anyway. A window could give the impression that the user's file was not saved because of the wrong date format. 
