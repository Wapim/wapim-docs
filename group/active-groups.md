---
description: This endpoint fetches active groups.
---

# Active Groups

{% api-method method="get" host="https://api.wapim.co/api/v1/whatsapp" path="/groups" %}
{% api-method-summary %}
Get Active Groups
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
Succesfully getting active groups.
{% endapi-method-response-example-description %}

```bash
{
	"status": true,
	"code": 200,
	"message": [
		{
			"gid": "15417543010-1570918620",
			"group_name": "Group Name 1"
		},
		{
			"gid": "16417543010-1578236320",
			"group_name": "Group Name 2"
		}
	]
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
	.get('https://api.wapim.co/api/v1/whatsapp/groups', {
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
  -X GET https://api.wapim.co/api/v1/whatsapp/groups \
  -H "token: YOUR_WAPIM_TOKEN"
```
{% endtab %}
{% endtabs %}

