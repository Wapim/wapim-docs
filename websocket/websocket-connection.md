---
description: You will learn about connection to Wapim WebSocket.
---

# WebSocket Connection

{% hint style="info" %}
You can use it only with **Platinum** plan.
{% endhint %}

{% hint style="warning" %}
Make sure to enable WebSocket in the Webhook settings on the [**Wapim Console**](https://app.wapim.io).
{% endhint %}

![Wapim Console webhook settings](../.gitbook/assets/wapim-whatsapp-websocket-options.png)

```markup
<html>
	<body>
		Hello Wapim WS
	</body>

	<script>
		let socket = new WebSocket('wss://api.wapim.io/ws?token=YOUR_WAPIM_TOKEN');

		socket.onopen = function(e) {
			console.log('[open] Connection established');
		};

		socket.onmessage = function(event) {
			console.log(`[message] Data received from server: ${event.data}`);
		};

		socket.onclose = function(event) {
			if (event.wasClean) {
				console.log(`[close] Connection closed cleanly, code=${event.code} reason=${event.reason}`);
			} else {
				// e.g. server process killed or network down
				// event.code is usually 1006 in this case
				console.log('[close] Connection died');
			}
		};

		socket.onerror = function(error) {
			console.log(`[error] ${error.message}`);
		};
	</script>
</html>
```

