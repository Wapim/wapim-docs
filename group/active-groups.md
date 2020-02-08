# Get Active Groups

{% api-method method="get" host="https://api.wapim.io/" path="api/v1/whatsapp/groups" %}
{% api-method-summary %}
Get Active Groups
{% endapi-method-summary %}

{% api-method-description %}
This endpoint get contacts.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Succesfully getting active groups.
{% endapi-method-response-example-description %}

```text
  {
    "status": true,
    "code": 200,
    "message": {
      "Active Groups": {
        "905320602911-1560716540": "Wapim.io",
        "905348372911-1563579554": "Merhaba Group"
      }
    }
  }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

