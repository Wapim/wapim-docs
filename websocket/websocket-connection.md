---
description: You will learn about Wapim WebSocket on this page.
---

# WebSocket

When you want to work real-time on the WhatsApp API, Wapim offers you a WebSocket connection. In this way, you can process all updates on your WhatsApp account in real time without any additional development.

{% hint style="info" %}
You can use this feature only with **Platinum** plan.
{% endhint %}

{% hint style="warning" %}
Make sure to enable WebSocket in the webhook settings on the [**Wapim Console**](https://app.wapim.io).
{% endhint %}

![Wapim Console webhook settings](../.gitbook/assets/wapim-whatsapp-websocket-options.png)

### Example Connection

We are preparing a very simple HTML document below. We create an event when the WebSocket connection is opened, a new message is received, the connection is closed, and for error cases.

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

### What situations do I get notified about?

You can learn about this on [**Webhook page**](https://docs.wapim.io/webhook/webhook).



