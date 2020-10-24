---
description: You can clear message queue with this endpoint.
---

# Clear Message Queue

{% api-method method="delete" host="https://api.wapim.co/api/v1/whatsapp" path="/queue" %}
{% api-method-summary %}
Clear Message Queue
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
	"message": 'All messages waiting in the queue have been deleted. OK..'
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
  .delete('https://api.wapim.co/api/v1/whatsapp/queue', {
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
  -X DELETE https://api.wapim.co/api/v1/whatsapp/queue \
  -H "token: YOUR_WAPIM_TOKEN"
```
{% endtab %}
{% endtabs %}

