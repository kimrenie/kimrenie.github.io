---
layout: post
title:  "S3. React App Wprkflow"
date:   2022-03-05 01:00:00 -0700
categories: senior design
---
<html><head><link rel="stylesheet" type="text/css" href="/../style2.css"></head><style>img {width: 75%}</style></html>

# What is React?

![react](/images/react.png)

React is a JavaScript library that serves to help a user develop and build a user interface. This user interface is pieced together with the use of `components` which are essentially snippets of code that React has the ability to update and re-render. Each of these components can work independently of each other and therefore the application of components is simple for the user to implement but also allows for React to isolate the component and create more complicated interfaces. 

These components can switch from being static to more interactive simply by changing content within a `render()` function.
The `state` of our component is initialized and stored through the usage of constructors named `this.state` and `setState`. More about this concept can be read from the sources in the References below. 

# 3 Working Parts

## Dependancy Management

Dependancy management in React can be achieved through the usage of libraries that are created through third parties. One of the most popular dependancy management tools is NPM (Node's Package Manager). NPM is a registry that has close to 1,000,000 different packages that are all contributed from open-source developers.

> SOme of the most popular NPM packages that are in use today are Express, React, Debug, etc.

## Bundlers

The creation of `modular code` is achieved through the usage of a bundler. A bundler takes multiple files and condenses them into a single file that is then referred to as a "bundle".

## Server

The usage of a server allows the React application to test and run the produced code onto the user's local computer. This NPM server must be kept running in order for changes to your app to be visually observed. 

# Main Folders

Some of the reoccuring files and folders that are found in React applications are as the following:

```
package.json - *This file contains the dependencies that the developer has chosen to utilize for this application.*
node_modules - *This folder contains all of the earlier referred to dependencies and scripts that need them.*
scr - *This folder contains the files that the React application directly works with.*
app.js - *This is a file that is automatically edited by the React workflow.*
app.css - *This is a file that determines the styling of the app.js file. 
etc.*

```

# References

Wikipedia [https://en.wikipedia.org/wiki/React_(JavaScript_library)] (https://en.wikipedia.org/wiki/React_(JavaScript_library)

Intro to React [https://reactjs.org/tutorial/tutorial.html#what-is-react] (https://reactjs.org/tutorial/tutorial.html#what-is-react)

React Workflow [https://www.pluralsight.com/guides/understanding-the-workflow-to-build-a-react-app] (https://www.pluralsight.com/guides/understanding-the-workflow-to-build-a-react-app)