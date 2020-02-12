# Contact List

{% api-method method="get" host="https://api.wapim.io/" path="api/v1/whatsapp/contacts" %}
{% api-method-summary %}
Get Information of Device
{% endapi-method-summary %}

{% api-method-description %}
This endpoint get contacts.
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
Succesfully getting contacts.
{% endapi-method-response-example-description %}

```text
[
  {
    "number": "15417543010",
    "pushname": "",
    "name": "James Smith",
    "group": false
  },
  {
    "number": "16417543010",
    "pushname": "Maria Garcia",
    "name": "",
    "group": false
  },
  {
    "number": "17417543010",
    "pushname": "",
    "name": "James Johnson",
    "group": false
  },
  ...
]
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
	.get('https://api.wapim.io/api/v1/whatsapp/contacts', {
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
  -X GET https://api.wapim.io/api/v1/whatsapp/contacts \
  -H "token: YOUR_WAPIM_TOKEN"
```
{% endtab %}
{% endtabs %}



