emitter
=======

A Mono module that will emit an event on the server side that contains the `link` object. This event will be listened by a custom script.

## How to use

### Configuration example

```JS
"emitter": {
    "module": "github/jillix/emitter/dev",
    "config": {},
    "operations": {
        "emit"      : {
            "roles": [0, 1],
            "params": [
                {
                    "eventName": "my event"
                }
            ]
        }
    }
}
```

while in the custom script we have:

```js
M.on("my event", function (link) {
    link.send(200, "Hello!");
});
```

## Changelog

### v0.4.0
 - transferred the module to the new jxMono organization
 - updated Bind to `v0.4.0`, Events to `v0.4.0`

### v0.3.1
 - Updated to Bind `v0.3.1`

### v0.3.0
 - Updated deps

### v0.2.3
 - Updated Events

### v0.2.2
 - Updated Events and Bind

### v0.2.1
 - Updated to Events v0.1.8

### v0.2.0
 - Added the client script
 - Added `Events` and `Bind` dependencies
 - Added `config.eventWhenReady` options

### v0.1.0
 - Initial release.
