# -Remove Participant from Group

{% api-method method="post" host="https://api.wapim.io/" path="api/v1/whatsapp/group/remove" %}
{% api-method-summary %}
Remove participant from group
{% endapi-method-summary %}

{% api-method-description %}
This endpoint remove participant from WhatsApp group.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="gid" type="string" required=true %}
Group ID
{% endapi-method-parameter %}

{% api-method-parameter name="participants" type="string" required=true %}
Phone numbers to be discarded from the group. You can separate with commas for multiple phone numbers. \(For example: 905546450000,905433468576\)
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Succesfully removed members from group.
{% endapi-method-response-example-description %}

```text
 {
    "status": true,
    "code": 201,
    "message": "The members were successfully removed from the group"
  }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

#### Example Usages

{% tabs %}
{% tab title="Node.js" %}
```coffeescript
const axios = require('axios');

axios
	.post(
		'https://api.wapim.io/api/v1/whatsapp/group/remove',
		{
			gid: 'GROUP_ID',
			participants: 'PHONE_NUMBER',
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
  -X POST https://api.wapim.io/api/v1/whatsapp/group/remove \
  -H "token: YOUR_WAPIM_TOKEN" \
  -d '{"participants": "PHONE_NUMBER", "gid":"GROUP_ID"}'
```
{% endtab %}
{% endtabs %}

