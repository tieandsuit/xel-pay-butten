This is a public open source project,  funded by XEL community.

usage:
```html
<head>
<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.3.2/jquery.min.js"></script>
<script type="text/javascript" src="xelbutton.php?includeJsFile=true"></script>
<script>
$( document ).ready(function() {
	$('xel_button').xelbutton({
		'recipient' : 'XEL-MAYC-ZZ3Y-YX56-6NH52',
		'server'  : 'xelbutton.php',
		'fee'     : '0.1',
		'amount'  : '1.0',
		'title'   : 'Example payment',
		'success' : function (hash, transaction) {
			console.log('Transaction1 is complete, transaction id '+transaction);
		}});
		$('xel_button2').xelbutton({
			'recipient' : 'XEL-MAYC-ZZ3Y-YX56-6NH52',
			'server'  : 'xelbutton.php',
			'fee'     : '0.1',
			'amount'  : '2.0',
			'title'   : 'Example payment 2',
			'mainButton': "images/pay_with_xel_gray.png",
			'success' : function (hash, transaction) {
				console.log('Transaction3 is complete, transaction id '+transaction);
		}});
});

	</script>
	</head>
	<body>
	<div id='xel_button'></div>
	<div id='xel_button2'></div>
</body>
```

If you want to use your own proxy server for XEL requests, here is the installation instructions:

first configure your config.json to fit your server.

Nodejs:
- npm install
- node server.js

PHP:
- please have these 4 files in same folder: xelbutton.php, config.json, crypto_browser.js xelbutton.js
- PHP needs curl
