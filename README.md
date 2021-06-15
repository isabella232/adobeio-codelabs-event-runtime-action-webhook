# Events Using Runtime Actions as Webhook
The codelab will guide you through how to consume events using runtime action as webhook. 

## Background

In previous codelab [here](https://adobeio-codelabs-journaling-events-adobedocs.hlx.page/?src=/README.html) we guide you through how to consume event using Journaling API
in this codelab, we will introduce another way to consume events - runtime action as webhook. This integration between Adobe I/O Runtime and I/O Events allow you create runtime actions to be setup as webhook endpoints on the Adobe developer console for receiving events, so that every time an event fires, your runtime action is executed 
and the debug tracking feature allow you to debug easily.  

## Benefits of using Runtime Action as Webhook

There are two main benefits to choose runtime action as webhook: 
- Built in Signature Verification 
- Tracing actions with Activation Ids 

## How to choose between Journaling API and Runtime Action webhook
- Journaling API: when you have a long running(async) actions that require guaranteed event handling especially when there is a surge of events, you should consider using the [journaling approach](https://adobeio-codelabs-journaling-events-adobedocs.hlx.page/?src=/README.html) for consuming events. 
- Runtime action webhook: If you have short-running action (that responds within 10 sec) we recommend setting up your runtime action as webhook

Now, let's begin our journey to this new feature ! 

Next lesson: [Requirements](lessons/requirements.md)