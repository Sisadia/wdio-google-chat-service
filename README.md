# wdio-google-chat-service

Webdriverio library to send test results as a slack notification/message to spaces do google chat.

## Installation

`npm install wdio-google-chat-service --save-dev`

or 

`yarn add wdio-google-chat-service`

## Configuration

At first, import the service to wdio config file `wdio.conf.js`

```
// wdio.conf.js
const slack = require('wdio-google-chat-service');
```

Para usar o serviço, você precisa ter o url do webhook do google chat para enviar a notificação e adicionar o url em 'webhook'

Example:

```
services: [[GoogleChatService, {
            webhook: 'https://chat.googleapis.com/v1/spaces/xxxxxxxxx/messages?key=xxxxxxxx&token=xxxxxxxxx',
            notifyOnlyOnFailure: false //Send notification only on test failure
        }]
],
```

## Features

- Support for mocha
- Error details
- Send notification only on test failure

## Results

![Test pass and fail](/wdio-google-chat-service/img/testPassAndFail.png)