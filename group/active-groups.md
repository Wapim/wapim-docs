# Active Groups

{% api-method method="get" host="https://api.wapim.io/api/v1/whatsapp" path="/groups" %}
{% api-method-summary %}
Get Active Groups
{% endapi-method-summary %}

{% api-method-description %}
This endpoint get active groups.
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

```text
  {
    "status": true,
    "code": 200,
    "message": {
      "Active Groups": {
        "15417543010-1560716540": "Wapim.io",
        "15417543011-1563579554": "Another Group"
      }
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
	.get('https://api.wapim.io/api/v1/whatsapp/groups', {
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
  -X GET https://api.wapim.io/api/v1/whatsapp/groups \
  -H "token: YOUR_WAPIM_TOKEN"
```
{% endtab %}
{% endtabs %}

