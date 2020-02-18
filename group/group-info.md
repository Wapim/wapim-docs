# -Group Informations

{% api-method method="post" host="https://api.wapim.io/api/v1/whatsapp" path="/group/info" %}
{% api-method-summary %}
Get Group Information
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
{% api-method-parameter name="gid" type="string" required=true %}
Group ID
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully getting info of groups.
{% endapi-method-response-example-description %}

```text
{
  "status": true,
  "code": 200,
  "message": {
    "jid": "",
    "owner": "15417543010@c.us",
    "subject": "Group Subject",
    "subjectTime": 1581596638,
    "subjectOwner": "15417543010",
    "desc": "Group Description",
    "descId": "1581960657-1048",
    "descTime": 1581990455,
    "descOwner": "15417543010",
    "creation": 1581596638,
    "status": 0,
    "participants": [
      {
        "id": "15417543010",
        "isAdmin": true,
        "isSuperAdmin": true
      },
      {
        "id": "16417543010",
        "isAdmin": false,
        "isSuperAdmin": false
      }
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
	.post(
		'https://api.wapim.io/api/v1/whatsapp/group/info',
		{
			gid: 'GROUP_ID',
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
  -X POST https://api.wapim.io/api/v1/whatsapp/group/info \
  -H "token: YOUR_WAPIM_TOKEN" \
  -d '{"gid": "GROUP_ID"}'
```
{% endtab %}
{% endtabs %}

