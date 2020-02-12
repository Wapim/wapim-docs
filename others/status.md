# Status

{% api-method method="get" host="https://api.wapim.io/api/v1/whatsapp" path="/status" %}
{% api-method-summary %}
Status
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Status successfully retrieved.
{% endapi-method-response-example-description %}

```
{
	"status": true,
	"code": 200,
	"message": {
		"Connected": true,
		"LoggedIn": true,
		"Idle": false,
		"phone_info": {
			"Battery": 49,
			"Platform": "iphone",
			"Connected": true,
			"Pushname": "John Doe",
			"Phone_number": "15417543010@c.us",
			"Lc": "US",
			"Phone": {
				"Mcc": "286",
				"Mnc": "002",
				"OsVersion": "12.4.4",
				"DeviceManufacturer": "Apple",
				"DeviceModel": "iPhone 5s",
				"OsBuildNumber": "undefined",
				"WaVersion": "2.20.21"
			},
			"Plugged": true,
			"Tos": 0,
			"Lg": "en",
			"Is_24_h": true
		}
	}
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



