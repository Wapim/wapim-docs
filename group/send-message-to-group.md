---
description: You can send messages to the groups with send message endpoints.
---

# Send Message to Group

{% hint style="info" %}
You will see the following text message example. But you can use all message endpoints in the same way.
{% endhint %}

{% api-method method="post" host="https://api.wapim.co/api/v1/whatsapp" path="/message/text" %}
{% api-method-summary %}
Send Message to Group
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
gid \(group id\)
{% endapi-method-parameter %}

{% api-method-parameter name="message" type="string" required=true %}
Content of text message.
{% endapi-method-parameter %}

{% api-method-parameter name="scheduled\_time" type="string" required=false %}
Schedule time. \(Timestamp\)
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
    'https://api.wapim.co/api/v1/whatsapp/message/text',
    {
     phone_number: 'GROUP_ID',
     message: 'Hello Group'
    },
    {
     headers: {
      token: 'YOUR_WAPIM_TOKEN',
     }
    }
  )
  .then(response => console.log(response.data))
  .catch(error => console.log(error.response.data));
```
{% endtab %}

{% tab title="cURL" %}
```bash
curl \
  -X POST https://api.wapim.co/api/v1/whatsapp/message/text \
  -H "token: YOUR_WAPIM_TOKEN" \
  -d '{"phone_number": "GROUP_ID", "message" : "Hello Group"}'
```
{% endtab %}
{% endtabs %}

