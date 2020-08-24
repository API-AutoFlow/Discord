# Summary
Integration with discord can be used to send alerts to users and channels to notify when certain events are triggered.

# API AutoFlow Version:
Configuration config.json was created using AutoFlow version __0.2.5__

# Need help?
Is you have questions about this example, feel free to post your question on the community "Ask Questions" website.

[Ask Questions](https://interactor.com/autoflow/questions){: .btn}

## Step 1. Create flow
* Create an HTTP Server
* Create an endpoint
  * NOTE: under properties the method must be POST
* From the right panel, press Action tab -> communication, Drag and drop HTTP-Request to the end of the flow
* From the right panel, press Action tab -> data, Drag and drop Set to the end of the flow

## Step 2. Setup Discord request body
Discord takes in HTTP request body as below

```
{
    "content": "Message content"
}
```

Use Data/Set action to create the object.

## Step 3. Discord API Call
### Communication/HTTP-request
#### Properties:
> * _url_:      NOTE: Paste the discord webhook
> * _Method_:   POST
> * _Body_:     Contents of what is being posted to discord. NOTE: May need to specify the content type as application json.  { “Content-Type”: “Application/JSON” }
> * _Header_:   blank
> * _Query_:    blank
> * _Timeout_:  Default

#### Output:
> * _Output-location_: Drag and drop the response body from right data panel


## Step 4. Test and Send Messages to your workspace

## Using Postman API Tester:
Select Method Post and Paste your discord http server. NOTE: Yours may differ
![Image](https://github.com/API-AutoFlow/discord-webhook/blob/master/img/1.png)

In the HTTP Request Header, insert the message you want to send. For example

> Hello World!

## Configuring Discord api webhook

#### Creating Webhook
https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks

#### Discord Message Format
https://birdie0.github.io/discord-webhooks-guide/discord_webhook.html
