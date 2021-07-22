# Events Using Runtime Actions as Webhook
The codelab will guide you through how to consume events using runtime action as webhook. 

## Background

In previous codelab [here](https://adobeio-codelabs-journaling-events-adobedocs.hlx.page/?src=/README.html) we guide you through how to consume event using Journaling API. In this codelab, we will introduce another way to consume events - runtime action as webhook. This integration between Adobe I/O Runtime and I/O Events allow you create runtime actions to be setup as webhook endpoints on the Adobe developer console for receiving events, so that every time an event fires, your runtime action is executed and the debug tracing feature allow you to debug easily.  

## Benefits of using Runtime Action as Webhook

There are two main benefits to choose runtime action as webhook: 
- Built in Signature Verification [read more](https://www.adobe.io/apis/experienceplatform/events/docs.html#!adobedocs/adobeio-events/master/webhook/runtime_webhooks.md#built-in-signature-verification)
- Tracing actions with Activation Ids 

## How to choose between Journaling API and Runtime Action webhook
- Journaling API: when you have a long running(async) actions that require guaranteed event handling especially when there is a surge of events, you should consider using the [journaling approach](https://adobeio-codelabs-journaling-events-adobedocs.hlx.page/?src=/README.html) to consume events. 
- Runtime action webhook: if you have short-running (sync) action for example, responds within 10 sec, we recommend setting up your runtime action as webhook

### Overview
This codelab will take you through the I/O events SYNC webhook registration using your own runtime actions via console.
As part of this codelab, we will cover all the behind the scene actions happening for the below 

- Using firefly template `publish-event`as custom event [click this](https://adobeio-codelabs-custom-events-adobedocs.project-helix.page/?src=/lessons/lesson1.html)
- Setting up event registration follow [this](https://adobeio-codelabs-custom-events-adobedocs.project-helix.page/?src=/lessons/lesson2.html)
- Ingesting subscribed events for that webhook in I/O Events pipeline
- Debug tracing on console for the Success and Failure scenarios

Next lesson: [Requirements](lessons/requirements.md)
