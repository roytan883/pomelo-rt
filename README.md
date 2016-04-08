## Pomelo -- a fast, scalable game server framework for node.js

Because the original pomelo rarely maintain, PR accept wait so long.
This is a modified version of Pomelo. Some bug fixing and features are list below:

* use pomelo-rpc-ws instead of pomelo-rpc, rpc performance increase from 2000/s to 4000/s
* use pomelo-admin-rt, fix pomelo-admin(which no longer maintaining) bug
 1. when master server die, the old pomelo-admin only try reconnect limit times. Later when master restart, the pomelo-admin will not connect to master. pomelo-admin-rt fix it to always try reconnect master server.
 2. when starting pomelo process, if there is no master server, then pomelo process will never try to connect master server, then the process can't use rpc forever. pomelo-admin-rt fix it to must connect master server before process running.

How to use it:
```
//var pomelo = require('pomelo-rt');
var pomelo = require('pomelo-rt');
```
