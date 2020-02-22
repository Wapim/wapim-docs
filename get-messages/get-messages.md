---
description: Fetches messages with a specific phone number or group.
---

# -Get Messages

{% api-method method="get" host="https://api.wapim.io/api/v1/whatsapp" path="/profile/device" %}
{% api-method-summary %}
Get Messages
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
Succesfully getting device info.
{% endapi-method-response-example-description %}

```text
{
    "Battery": 43,
    "Platform": "smbi",
    "Connected": true,
    "Pushname": "John Doe",
    "Wid": "15417543010@c.us",
    "Lc": "US",
    "Phone": {
      "Mcc": "286",
      "Mnc": "001",
      "OsVersion": "12.1.4",
      "DeviceManufacturer": "Apple",
      "DeviceModel": "iPhone 7",
      "OsBuildNumber": "undefined",
      "WaVersion": "2.19.121"
    },
    "Plugged": false,
    "Tos": 0,
    "Lg": "en",
    "Is24h": true
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
		'https://api.wapim.io/api/v1/whatsapp/chat',
		{
			phone_number: 'PHONE_NUMBER_OR_GROUP_ID',
			count: 10,
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
  -X POST https://api.wapim.io/api/v1/whatsapp/chat \
  -H "token: YOUR_WAPIM_TOKEN" \
  -d '{"phone_number": "PHONE_NUMBER_OR_GROUP_ID", "count": 10}'
```
{% endtab %}
{% endtabs %}

