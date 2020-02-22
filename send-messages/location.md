---
description: You can send WhatsApp location messages with this endpoint.
---

# Location

{% api-method method="post" host="https://api.wapim.io/api/v1/whatsapp" path="/message/location" %}
{% api-method-summary %}
Send Location
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

{% api-method-parameter name="lat" type="float" required=true %}
Latitude. \(Example: 37.757815\)
{% endapi-method-parameter %}

{% api-method-parameter name="lon" type="float" required=true %}
Longitude. \(Example: -122.5076401\)
{% endapi-method-parameter %}

{% api-method-parameter name="title" type="string" required=false %}
Message caption.
{% endapi-method-parameter %}

{% api-method-parameter name="scheduled\_time" type="string" required=false %}
Scheduled time. \(Timestamp\)
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Location has been successfully submitted.
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
        'https://api.wapim.io/api/v1/whatsapp/message/location',
        {
            phone_number: 'RECIPIENT_NUMBER',
            lat: 37.757815,
            lon: -122.5076401,
            title: 'My Location',
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
  -X POST https://api.wapim.io/api/v1/whatsapp/message/location \
  -H "token: YOUR_WAPIM_TOKEN" \
  -d '{"phone_number": "RECIPIENT_NUMBER", "lat": 37.757815, "lon": -122.5076401, "title": "My Location"}'
```
{% endtab %}
{% endtabs %}

