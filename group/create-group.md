---
description: With this endpoint you can create a new WhatsApp group.
---

# Create New Group

{% api-method method="post" host="https://api.wapim.co/api/v1/whatsapp" path="/group/create" %}
{% api-method-summary %}
Create a new WhatsApp Group
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
{% api-method-parameter name="subject" type="string" required=true %}
The subject of the group
{% endapi-method-parameter %}

{% api-method-parameter name="participants" type="string" required=true %}
Phone numbers to be added to the group. You can separate with commas for multiple phone numbers. \(For example: 905546450000,905433468576\)
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Succesfully created group.
{% endapi-method-response-example-description %}

```text
 {
    "status": true,
    "code": 201,
    "message": "The group was successfully created."
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
		'https://api.wapim.co/api/v1/whatsapp/group/create',
		{
			subject: 'Welcome to Wapim!',
			participants: 'WHATSAPP_NUMBER_1,WHATSAPP_NUMBER_2',
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
  -X POST https://api.wapim.co/api/v1/whatsapp/group/create \
  -H "token: YOUR_WAPIM_TOKEN" \
  -d '{"subject": "Welcome to Wapim!", "participants":"WHATSAPP_NUMBER_1,WHATSAPP_NUMBER_2"}'
```
{% endtab %}
{% endtabs %}

