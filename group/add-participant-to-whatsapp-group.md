# -Add Participant to Group

{% api-method method="post" host="https://api.wapim.io/" path="api/v1/whatsapp/group/add" %}
{% api-method-summary %}
Add participant to group
{% endapi-method-summary %}

{% api-method-description %}
This endpoint add participant to WhatsApp group.
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
Phone numbers to be added to the group. You can separate with commas for multiple phone numbers. \(For example: 905546450000,905433468576\)
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Succesfully added members to group.
{% endapi-method-response-example-description %}

```text
 {
    "status": true,
    "code": 201,
    "message": "The members were successfully added to the group"
  }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

