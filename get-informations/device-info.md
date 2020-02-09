# Device Info

{% api-method method="get" host="https://api.wapim.io/" path="api/v1/whatsapp/profile/device" %}
{% api-method-summary %}
Get Information of Device
{% endapi-method-summary %}

{% api-method-description %}
This endpoint get device info.
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
    "Pushname": "WAPIM",
    "Wid": "15417543010@c.us",
    "Lc": "TR",
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

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Unverifiable parameters.
{% endapi-method-response-example-description %}

```text
{
   "status":false,
   "code":400,
   "message":"Bad Request",
   "error":{
      "Send Text":[
         "Malformed or missing phone id or message data!"
      ]
   }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% tabs %}
{% tab title="Node.js" %}
```coffeescript
const axios = require('axios');

axios
	.get('https://api.wapim.io/api/v1/whatsapp/profile/device', {
		headers: {
			token: 'YOUR_WAPIM_TOKEN',
		},
	})
	.then(response => console.log(response.data))
	.catch(error => console.log(error.response.data));
```
{% endtab %}

{% tab title="cURL" %}
```
curl \ 
 -X GET https://api.wapim.io/api/v1/whatsapp/profile/device \
 -H "token: YOUR_WAPIM_TOKEN"
```
{% endtab %}
{% endtabs %}

