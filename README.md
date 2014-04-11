#Thunderpush JS Client


##Usage

```javascript
// Connect to server
Thunder.connect(
  "localhost:8080",        // host:port
  "key",                   // key
  ["test"],                // base channels to subscribe
  {
    log: true,             // enable logging
    user: 'somerandomid'   // user id
  }
);

// Disconnect from server
Thunder.disconnect();

///Listen to messages
Thunder.listen(function(data) {});

// Subscribe to channel
Thunder.subscribe(channelName, successCallback, errorCallback);

// Unsubscribe to channel
Thunder.unsubscribe(channelName, successCallback, errorCallback);

// Channels subscribed to
Thunder.channels;

//-- Events

// On sock open
Thunder.onSockOpen(callback)

// On sock error
Thunder.onSockError(callback)

// On sock message
Thunder.onSockMessage(callback)

```
