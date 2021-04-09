node-red-contrib-korbitpublic
================

Node-RED node for korbitpublic



## Install

To install the stable version use the `Menu - Manage palette - Install`
option and search for node-red-contrib-korbitpublic, or run the following
command in your Node-RED user directory, typically `~/.node-red`

    npm install node-red-contrib-korbitpublic

## Wrapper korbit public API
- https://apidocs.korbit.co.kr/

## Sample parameters
```js

msg.params = {};
msg.params.currency_pairs = 'btc_krw'
return msg;

```

## Sample flows
```json
[{"id":"19362bad.7e77b4","type":"korbitpublic","z":"56254b54.9f4f14","name":"ticker","api":"ticker","currency_pair":"btc_krw","x":410,"y":40,"wires":[["519b02ca.4b175c"]]},{"id":"c220679c.1aefa8","type":"inject","z":"56254b54.9f4f14","name":"","props":[{"p":"payload"},{"p":"topic","vt":"str"}],"repeat":"","crontab":"","once":false,"onceDelay":0.1,"topic":"","payload":"","payloadType":"date","x":120,"y":40,"wires":[["f77526f6.fba1b8"]]},{"id":"f77526f6.fba1b8","type":"function","z":"56254b54.9f4f14","name":"","func":"\nreturn msg;","outputs":1,"noerr":0,"initialize":"","finalize":"","x":260,"y":40,"wires":[["19362bad.7e77b4"]]},{"id":"519b02ca.4b175c","type":"debug","z":"56254b54.9f4f14","name":"","active":true,"tosidebar":true,"console":false,"tostatus":false,"complete":"false","statusVal":"","statusType":"auto","x":650,"y":40,"wires":[]},{"id":"f5f52e99.2ea1","type":"korbitpublic","z":"56254b54.9f4f14","name":"ticker/detailed","api":"ticker/detailed","currency_pair":"btc_krw","x":440,"y":80,"wires":[["61a017bc.671788"]]},{"id":"1d6f8af3.d80585","type":"inject","z":"56254b54.9f4f14","name":"","props":[{"p":"payload"},{"p":"topic","vt":"str"}],"repeat":"","crontab":"","once":false,"onceDelay":0.1,"topic":"","payload":"","payloadType":"date","x":120,"y":80,"wires":[["a12b9893.c165c8"]]},{"id":"a12b9893.c165c8","type":"function","z":"56254b54.9f4f14","name":"","func":"\nreturn msg;","outputs":1,"noerr":0,"initialize":"","finalize":"","x":260,"y":80,"wires":[["f5f52e99.2ea1"]]},{"id":"61a017bc.671788","type":"debug","z":"56254b54.9f4f14","name":"","active":true,"tosidebar":true,"console":false,"tostatus":false,"complete":"false","statusVal":"","statusType":"auto","x":650,"y":80,"wires":[]},{"id":"164723ae.83528c","type":"korbitpublic","z":"56254b54.9f4f14","name":"ticker/detailed/all","api":"ticker/detailed/all","currency_pair":"btc_krw","x":450,"y":120,"wires":[["cfcdcdf0.addbb"]]},{"id":"31b0048d.7c66cc","type":"inject","z":"56254b54.9f4f14","name":"","props":[{"p":"payload"},{"p":"topic","vt":"str"}],"repeat":"","crontab":"","once":false,"onceDelay":0.1,"topic":"","payload":"","payloadType":"date","x":120,"y":120,"wires":[["6430644.622219c"]]},{"id":"6430644.622219c","type":"function","z":"56254b54.9f4f14","name":"","func":"\nreturn msg;","outputs":1,"noerr":0,"initialize":"","finalize":"","x":260,"y":120,"wires":[["164723ae.83528c"]]},{"id":"cfcdcdf0.addbb","type":"debug","z":"56254b54.9f4f14","name":"","active":true,"tosidebar":true,"console":false,"tostatus":false,"complete":"false","statusVal":"","statusType":"auto","x":650,"y":120,"wires":[]},{"id":"c78994c4.9b4bc8","type":"korbitpublic","z":"56254b54.9f4f14","name":"orderbook","api":"orderbook","currency_pair":"btc_krw","x":420,"y":160,"wires":[["4121b0e.5d5355"]]},{"id":"99dea668.aa2b98","type":"inject","z":"56254b54.9f4f14","name":"","props":[{"p":"payload"},{"p":"topic","vt":"str"}],"repeat":"","crontab":"","once":false,"onceDelay":0.1,"topic":"","payload":"","payloadType":"date","x":120,"y":160,"wires":[["1b7c4e8b.3b2a01"]]},{"id":"1b7c4e8b.3b2a01","type":"function","z":"56254b54.9f4f14","name":"","func":"\nreturn msg;","outputs":1,"noerr":0,"initialize":"","finalize":"","x":260,"y":160,"wires":[["c78994c4.9b4bc8"]]},{"id":"4121b0e.5d5355","type":"debug","z":"56254b54.9f4f14","name":"","active":true,"tosidebar":true,"console":false,"tostatus":false,"complete":"false","statusVal":"","statusType":"auto","x":650,"y":160,"wires":[]},{"id":"5d447484.f718ec","type":"korbitpublic","z":"56254b54.9f4f14","name":"transactions","api":"transactions","currency_pair":"btc_krw","x":430,"y":200,"wires":[["4ff1f29c.b15a5c"]]},{"id":"25df1cf9.ece074","type":"inject","z":"56254b54.9f4f14","name":"","props":[{"p":"payload"},{"p":"topic","vt":"str"}],"repeat":"","crontab":"","once":false,"onceDelay":0.1,"topic":"","payload":"","payloadType":"date","x":120,"y":200,"wires":[["242e48ba.460ab8"]]},{"id":"242e48ba.460ab8","type":"function","z":"56254b54.9f4f14","name":"","func":"\nreturn msg;","outputs":1,"noerr":0,"initialize":"","finalize":"","x":260,"y":200,"wires":[["5d447484.f718ec"]]},{"id":"4ff1f29c.b15a5c","type":"debug","z":"56254b54.9f4f14","name":"","active":true,"tosidebar":true,"console":false,"tostatus":false,"complete":"false","statusVal":"","statusType":"auto","x":650,"y":200,"wires":[]},{"id":"d23ffd73.eea55","type":"korbitpublic","z":"56254b54.9f4f14","name":"constants","api":"constants","currency_pair":"btc_krw","x":420,"y":240,"wires":[["1cced98c.631156"]]},{"id":"1ab8250f.d2103b","type":"inject","z":"56254b54.9f4f14","name":"","props":[{"p":"payload"},{"p":"topic","vt":"str"}],"repeat":"","crontab":"","once":false,"onceDelay":0.1,"topic":"","payload":"","payloadType":"date","x":120,"y":240,"wires":[["c3c96016.d9eef"]]},{"id":"c3c96016.d9eef","type":"function","z":"56254b54.9f4f14","name":"","func":"\nreturn msg;","outputs":1,"noerr":0,"initialize":"","finalize":"","x":260,"y":240,"wires":[["d23ffd73.eea55"]]},{"id":"1cced98c.631156","type":"debug","z":"56254b54.9f4f14","name":"","active":true,"tosidebar":true,"console":false,"tostatus":false,"complete":"false","statusVal":"","statusType":"auto","x":650,"y":240,"wires":[]}]
```

## Sample result
```json
{"timestamp":1617938271435,"last":"74504000","open":"71409000","bid":"74408500","ask":"74532000","low":"70430500","high":"75890000","volume":"469.76881894","change":"3095000","changePercent":"4.33"}
```
