# Send Text Message

{% api-method method="post" host="https://api.wapim.io/" path="api/v1/whatsapp/message/text" %}
{% api-method-summary %}
Send Text Message
{% endapi-method-summary %}

{% api-method-description %}
This endpoint sends an text message.
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
A phone number starting with the country code.
{% endapi-method-parameter %}

{% api-method-parameter name="message" type="string" required=true %}
Content of text message
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Succesfully sended text message.
{% endapi-method-response-example-description %}

```text
{
    "queue_message_id": "905546453273_997B21D0C8B90189041D",
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
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

