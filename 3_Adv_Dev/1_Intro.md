#This should include text from another page

<head>
	<link rel="import" href="http://ble-intros.readthedocs.org/en/latest/GettingStarted/DesignersIntro/#mbed">
</head>

<body>
<script>
	var link - document.querySelector('link[rel="import"]');
	var content = link.import;
	var el = content.querySelect('.warning');
	document.body.appendChild(el.cloneNode(true));
</script>
</body>