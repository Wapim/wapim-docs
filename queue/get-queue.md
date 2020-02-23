---
description: Fetches chat history with a specific phone number or group.
---

# Get Queue

{% api-method method="get" host="https://api.wapim.io/api/v1/whatsapp" path="/queue" %}
{% api-method-summary %}
Get Queue
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
Successfully getting chat history.
{% endapi-method-response-example-description %}

```text

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Example Usages

{% tabs %}
{% tab title="Node.js" %}
```coffeescript

```
{% endtab %}

{% tab title="cURL" %}
```bash
curl \
  -X GET https://api.wapim.io/api/v1/whatsapp/queue \
  -H "token: YOUR_WAPIM_TOKEN"
```
{% endtab %}
{% endtabs %}

