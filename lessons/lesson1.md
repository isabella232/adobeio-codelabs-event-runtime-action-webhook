## Lesson 1: Setup and Overview

### Setup 
First, let's assume you already have basic knowledge about Project Firefly and how to create a project through Adobe Developer Console using template. Follow this[here](https://www.adobe.io/apis/experienceplatform/runtime/docs.html#!adobedocs/adobeio-runtime/master/getting-started/setup.md) to setup your cli with Runtime plugin which is required as pre-requisite. The runtime cli will enable you create a runtime action and hook it up with an integration via Adobe Developer Console. 


### Overview
This POC will take you through the I/O events SYNC webhook registration using your own runtime actions via console.
As part of this POC, we will cover all the behind the scene actions happening for the below 

- As an user, creating my own runtime action (having the business logic)
-  Setting up event registration using this user-defined runtime action on console and get a SYNC webhook
- Ingesting subscribed events for that webhook in I/O Events pipeline
- Showing how the signature validation is done 
- Debug tracing on console for the Success and Failure scenarios
- Event registration deletion - what actually gets deleted

Next lesson: [Step by step guide](lesson2.md)