---
description: Fetches latest messages.
---

# Last Messages

{% api-method method="post" host="https://api.wapim.io/api/v1/whatsapp" path="/lastmessages" %}
{% api-method-summary %}
Last Messages
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
{% api-method-parameter name="count" type="number" required=false %}
How many messages. \(Default: 10\)
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Succesfully getting chat history.
{% endapi-method-response-example-description %}

```text
{
   "status":true,
   "code":200,
   "message":[
      {
         "event_name":"TextMessage",
         "from_group":false,
         "from_me":true,
         "from_phone_number":"15417543010",
         "instance_id":"ck6w8bq3n05hg07995ztv1a33",
         "message_id":"3EB01FB9705FB29BC6EA",
         "text":"Hi",
         "timestamp":1582288548,
         "to_phone_number":"16417543016"
      },
      {
         "event_name":"TextMessage",
         "from_group":false,
         "from_me":false,
         "from_phone_number":"16417543016",
         "instance_id":"ck6w8bq3n05hg07995ztv1a33",
         "message_id":"3EB0120269FB6738F850",
         "text":"How are you?",
         "timestamp":1582288581,
         "to_phone_number":"15417543010"
      },
      {
         "event_name":"TextMessage",
         "from_group":false,
         "from_me":false,
         "from_phone_number":"16417543016",
         "instance_id":"ck6w8bq3n05hg07995ztv1a33",
         "message_id":"3A06FC2CCEC0E2122006",
         "text":"Fine. You?",
         "timestamp":1582291178,
         "to_phone_number":"15417543010"
      }
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
  .post(
    'https://api.wapim.io/api/v1/whatsapp/lastmessages',
    {
      count: 2,
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
  -X POST https://api.wapim.io/api/v1/whatsapp/lastmessages \
  -H "token: YOUR_WAPIM_TOKEN" \
  -d '{"count": 2}'
```
{% endtab %}
{% endtabs %}

