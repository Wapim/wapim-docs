---
description: You can send WhatsApp video messages with this endpoint.
---

# Video

{% api-method method="post" host="https://api.wapim.io/api/v1/whatsapp" path="/message/video" %}
{% api-method-summary %}
Send Video Message
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

{% api-method-parameter name="content\_url" type="string" required=true %}
Content URL. \(**Max. 5mb**\)
{% endapi-method-parameter %}

{% api-method-parameter name="caption" type="string" required=false %}
Text under the video.
{% endapi-method-parameter %}

{% api-method-parameter name="scheduled\_time" type="number" required=false %}
Schedule time. \(Timestamp\)
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Video successfully retrieved.
{% endapi-method-response-example-description %}

```text
{
   "queue_message_id":"15417543010_B00C430369960C50285A",
   "message":"We reached successfully"
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
		'https://api.wapim.io/api/v1/whatsapp/message/video',
		{
			phone_number: 'RECIPIENT_NUMBER',
			content_url: 'https://sample-videos.com/video123/mp4/720/big_buck_bunny_720p_1mb.mp4',
			caption: 'Hello from Wapim',
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
  -X POST https://api.wapim.io/api/v1/whatsapp/message/video \
  -H "token: YOUR_WAPIM_TOKEN" \
  -d '{"phone_number": "RECIPIENT_NUMBER", "content_url":"https://sample-videos.com/video123/mp4/720/big_buck_bunny_720p_1mb.mp4",  "caption" : "Hello from Wapim"}'
```
{% endtab %}
{% endtabs %}

