---
description: You can send WhatsApp image messages with this endpoint.
---

# Image

{% api-method method="post" host="https://api.wapim.io/" path="api/v1/whatsapp/message/image" %}
{% api-method-summary %}
Send Image Message
{% endapi-method-summary %}

{% api-method-description %}
This endpoint send an image message.
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

{% api-method-parameter name="content\_url" type="string" required=true %}
Content URL. \(**Max. 5mb**\)
{% endapi-method-parameter %}

{% api-method-parameter name="caption" type="string" required=false %}
Text under the image.
{% endapi-method-parameter %}

{% api-method-parameter name="scheduled\_time" type="string" required=false %}
Schedule time \(Timestamp\)
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
    "queue_message_id": "905546453474_997B21D0C8B90189041D",
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

{% api-method-response-example httpCode=413 %}
{% api-method-response-example-description %}
Big image file!
{% endapi-method-response-example-description %}

```text
{
    "status": false,
    "code": 413,
    "message": "Big file",
    "error": "Max 5 MB file."
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
    'https://api.wapim.io/api/v1/whatsapp/message/image',
    {
      phone_number: 'Recipient Number',
      content_url: 'https://i.picsum.photos/id/859/800/600.jpg',
      caption: 'Hello from Wapim'
    },
    {
      headers: {
       token: 'YOUR WAPIM TOKEN',
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
  -X POST https://api.wapim.io/api/v1/whatsapp/message/image \
  -H "token: YOUR WAPIM TOKEN" \
  -d '{"phone_number": "Recipient Number", "content_url":"https://i.picsum.photos/id/859/800/600.jpg",  "caption" : "Hello from Wapim"}'
```
{% endtab %}
{% endtabs %}

