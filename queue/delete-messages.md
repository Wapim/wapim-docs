# Clear Message Queue

---
description: You can receive your message id list in the queue with this endpoint.
---

{% api-method method="get" host="https://api.wapim.io/api/v1/whatsapp" path="/queue" %}
{% api-method-summary %}
Get Queue
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully fetches queue.
{% endapi-method-response-example-description %}

```text
{
	"status": true,
	"code": 200,
	"message": [
		"15417543010_336DB0ABD8A3DD6D7811",
		"15417543010_2AF15D005763B87F5F95",
		"15417543010_739FA20C28DF17160616",
		"15417543010_D26C90A6EC4A84619B75",
		"15417543010_47FB14667D176D7A14F1"
	]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Example Usages

{% tabs %}
{% tab title="Node.js" %}
```coffeescript
const axios = require('axios');

axios
	.get('https://api.wapim.io/api/v1/whatsapp/queue', {
		headers: {
			token: 'YOUR_WAPIM_TOKEN',
		},
	})
	.then(response => console.log(response.data))
	.catch(error => console.log(error.response.data));

```
{% endtab %}

{% tab title="cURL" %}
```bash
curl \
  -X GET https://api.wapim.io/api/v1/whatsapp/queue \
  -H "token: YOUR_WAPIM_TOKEN"
```
{% endtab %}
{% endtabs %}

