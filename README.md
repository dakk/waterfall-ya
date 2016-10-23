# Yet Another Waterfall library for node

waterfall-ya implements a waterfall utility to avoid (callback hell)[http://callbackhell.com/]. It doesn't require
any external dependencies.


## Install

``` npm install waterfall-ya ```


## Usage

```javascript
	var waterfall = require ('waterfall-ya');
	
	waterfall ([
		function (next) {
			someAsyncTask (a, b, next);
		},
		function (err, data, next) {
			// data contains someAsyncTask result
			someOtherAsyncTask (data, next);		
		},
		function (err, data, next) {
			// data contains someOtherAsyncTask result
			someOtherAsyncTask2 (data, next);		
		},
		function (err, data) {
			console.log ('All done.', data);
		}
	]);
```


