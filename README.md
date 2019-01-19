# TinyWebExt BrowserCommunication

A tiny wrapper around the browser.runtime.onMessage, so you have a message type to separate different messages.

## Message Types

The message types itself shall be hardcoded and are thus saved in a file called `BrowserCommunicationTypes.js` in the `data` directory in parent directory of this module, just like this:

```
.
├── BrowserCommunication
│   ├── BrowserCommunication.js
│   ├── CONTRIBUTORS
│   ├── LICENSE.md
│   ├── README.md
│   └── ...
├── data
│   ├── BrowserCommunicationTypes.js
│   └── ...
...
```

Inside of it, just export a static constant `COMMUNICATION_MESSAGE_TYPE` with an object of all message types, with an internal ID to actually pass.
An example of the `BrowserCommunicationTypes.js` is saved in [`examples/BrowserCommunicationTypes.js`](examples/BrowserCommunicationTypes.js).

## Adding listeners

The only important function is basically `BrowserCommunication.addListener`. 
Just pass to it a set-up [message type](#message-types) and a callback to actually register. For the former, it is obviously recommend to use the constant from there and pass it into the function.

You can register as many listeners for one message type, as you want.

## Removing listeners

[Still TODO...](https://github.com/TinyWebEx/BrowserCommunication/issues/2)
