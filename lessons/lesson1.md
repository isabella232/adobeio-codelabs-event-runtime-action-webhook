## Lesson 1: Step by Step Guide

### Initialize a Firefly app using template 
If you don't have a Firefly app, please follow [this](https://adobeio-codelabs-custom-events-adobedocs.project-helix.page/?src=/lessons/lesson1.html) to create one, make sure you have `publish-event`in the template and add `I/O management API`in console. After done, and run `aio app deploy` you should have seen this 
![publishevent](assets/publishevent-1.png)

and here is the project I set up at adobe developer console 
![consoleproject](assets/console-project-2.png)

### Event Registration

- Follow the [this](https://adobeio-codelabs-custom-events-adobedocs.project-helix.page/?src=/lessons/lesson2.html) to register the event provider, in my case, while at the step of 
```
aio event registration create 
``` 
It will show you a sample of JSON format, make sure you select `webhook` in my case, here is an example of .json file
```
{
    "name": "event-runtime-integration",
    "description": "test event runtime",
    "delivery_type": "WEBHOOK",
    "webhook_url": "https://io-webhook.herokuapp.com/webhook/testjie",
    "events_of_interest": [
        {
        "provider_id": "ccefc74d-9696-4b99-a799-f2d34a4189cd",
        "event_code": "eventrt"
        }
    ]
}
```

- After finish the steps above, you should be able to see in your terminal that you successfully create register the event, and you will also see it in at adobe developer console under the left bottom corner `event` your registration provider `eventrt` show up there. 
![console-event](assets/console-event-3.png)


### Event Runtime Integration 

- With all above setup, now you get your `providerId`, `eventCode`, you can go back to your firefly App trying to invoke a custom event like below: 
![invoke-event](assets/event-invoke-4.png)

- You should see this runtime action created in the `user defined actions` 
![user-define-action](assets/user-define-action-5.png)

- User now adds the event api to the project to setup the event registration
![add-event](assets/add-event-6.png)

- Adding from our custom event provider we just registered `eventruntime` (you should be able to see your register event in this list)
![add-event](assets/add-event-7.png)

- Subscribing to the "eventrt" event type
![add-event](assets/add-event-8.png)

- Generate the JWT service account credentials key pair
![add-event](assets/add-event-9.png)

- On the registration details page provide name and select the runtime user action created to setup event registration, select the user action from the dropdown of Runtime Actions 
![add-event](assets/add-event-10.png)

Now, clicking on the "save configured events", then if we go to dev console we see this new "eventrt" - with new sync event handler as webhook registered successfully
![add-event](assets/add-event-11.png)

Now, if user goes to his aio-cli and do "aio runtime list", he can see the below entities created as part of the new flow of event registration
![add-event](assets/add-event-12.png)

Next lesson: [Verify the result](lesson3.md)