# Profile Photos

{% api-method method="post" host="https://api.wapim.io/api/v1/whatsapp" path="/profilephoto" %}
{% api-method-summary %}
Get Information of Device
{% endapi-method-summary %}

{% api-method-description %}
This endpoint get contacts.
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
A phone number starting with the country code. You should set group id for group photos.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Succesfully getted profile photo.
{% endapi-method-response-example-description %}

```text
 {
    "status": true,
    "code": 200,
    "message": {
      "eurl": "https://cdn.wapim.io/wapim-media/profilepictures/requested_number.jpg",
      "tag": "",
      "status": 0
    }
  }
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
Requested photo is blocked or no photo for this number.
{% endapi-method-response-example-description %}

```text
 {
    "status": true,
    "code": 403,
    "message": "Permission denied"
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
		'https://api.wapim.io/api/v1/whatsapp/profilephoto',
		{
			phone_number: 'PHONE_NUMBER',
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
  -X POST https://api.wapim.io/api/v1/whatsapp/profilephoto \
  -H "token: YOUR_WAPIM_TOKEN" \
  -d '{"phone_number": "PHONE_NUMBER"}'
```
{% endtab %}
{% endtabs %}

