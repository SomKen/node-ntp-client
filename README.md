# ntp-client [![Build Status](https://secure.travis-ci.org/moonpyk/node-ntp-client.png?branch=master)](http://travis-ci.org/moonpyk/node-ntp-client)

Pure Javascript implementation of the NTP Client Protocol

## Getting Started
Install the module with: `npm install ntp-client`

## Examples
### Get just the time
```javascript
var ntpClient = require('ntp-client');

ntpClient.getNetworkTime("pool.ntp.org", 123, function(err, date) {
    if(err) {
        console.error(err);
        return;
    }

    console.log("Current time : ");
    console.log(date); // Mon Jul 08 2013 21:31:31 GMT+0200 (Paris, Madrid (heure d’été))
});
```

### Get the time and the server's stratum
Get the server's startum:
```javascript
var ntpClient = require('ntp-client');

ntpClient.getNetworkTime("pool.ntp.org", 123, function(err, date, stratum) {
    if(err) {
        console.error(err);
        return;
    }

    console.log("Current time : ");
    console.log(date); // Mon Jul 08 2013 21:31:31 GMT+0200 (Paris, Madrid (heure d’été))
    console.log("Current stratum : "); 
    console.log(stratum); // 3
});
```

## Contributors
 * Clément Bourgeois (https://github.com/moonpyk)
 * Callan Bryant (https://github.com/naggie)
 * SomKen (https://github.com/somken)

## License
Copyright (c) 2014 Clément Bourgeois
Licensed under the MIT license.

