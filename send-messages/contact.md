---
description: You can send WhatsApp contact messages with this endpoint.
---

# Contact

{% api-method method="post" host="https://api.wapim.io/api/v1/whatsapp" path="/message/contact" %}
{% api-method-summary %}
Send Contact Message
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
A phone number starting with the country code. US Example \(15417543010\).
{% endapi-method-parameter %}

{% api-method-parameter name="contact\_name" type="string" required=true %}
Contact name.
{% endapi-method-parameter %}

{% api-method-parameter name="contact\_number" type="string" required=true %}
Contact number.
{% endapi-method-parameter %}

{% api-method-parameter name="scheduled\_time" type="string" required=false %}
Scheduled time. \(Timestamp\)
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully send image message.
{% endapi-method-response-example-description %}

```text
{
    "queue_message_id": "15417543010_997B21D0C8B90189041D",
    "message": "We reached successfully"
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
	.post(
		'https://api.wapim.io/api/v1/whatsapp/message/contact',
		{
			phone_number: 'RECIPIENT_NUMBER',
			contact_name: 'CONTACT_NAME',
			contact_number: 'CONTACT_NUMBER',
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
  -X POST https://api.wapim.io/api/v1/whatsapp/message/contact \
  -H "token: YOUR_WAPIM_TOKEN" \
  -d '{"phone_number":"RECIPIENT_NUMBER", "contact_name":"CONTACT_NAME", "contact_number":"CONTACT_NUMBER"}'
```
{% endtab %}
{% endtabs %}

