---
description: You can send WhatsApp link messages with this endpoint.
---

# Link

{% api-method method="post" host="https://api.wapim.io/api/v1/whatsapp" path="/message/link" %}
{% api-method-summary %}
Send Link Message
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

{% api-method-body-parameters %}
{% api-method-parameter name="phone\_number" type="string" required=true %}
A phone number starting with the country code. US example: "15417543010".
{% endapi-method-parameter %}

{% api-method-parameter name="url" type="string" required=true %}
Link of website.
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="string" required=false %}
Link description.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully send text message.
{% endapi-method-response-example-description %}

```text
{
    "queue_message_id": "15417543010_997B21D0C8B90189041D",
    "message": "We reached successfully"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Missing or wrong params!
{% endapi-method-response-example-description %}

```text
{
    "status": false,
    "code": 400,
    "message": "Bad Request",
    "error": {
        "Send Text": [
            "Malformed or missing phone id or message data!"
        ]
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

### Example Usages

{% tabs %}
{% tab title="Node.js" %}
```coffeescript
const axios = require('axios');

axios
	.post(
		'https://api.wapim.io/api/v1/whatsapp/message/link',
		{
			phone_number: 'RECIPIENT_NUMBER',
			url: 'https://wapim.io',
			title: 'WAPIM',
			description: 'Super fast WhatsApp API!',
		},
		{
			headers: {
				token: 'YOUR_WAPIM_TOKEN',
			},
		},
	)
	.then(response => console.log(response.data))
	.catch(error => console.log(error.response.data));
```
{% endtab %}

{% tab title="cURL" %}
```bash
curl \
  -X POST https://api.wapim.io/api/v1/whatsapp/message/link \
  -H "token: YOUR_WAPIM_TOKEN" \
  -d '{"phone_number": "RECIPIENT_NUMBER", "url": "https://wapim.io", "title": "WAPIM", "description": "Super fast WhatsApp API!"}'
```
{% endtab %}
{% endtabs %}

