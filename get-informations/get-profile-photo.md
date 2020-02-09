# Profile Photos

{% api-method method="get" host="https://api.wapim.io/" path="api/v1/whatsapp/profilephoto" %}
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
A phone number starting with the country code.
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

{% tabs %}
{% tab title="Node.js" %}
```text

```
{% endtab %}

{% tab title="cURL" %}
```

```
{% endtab %}
{% endtabs %}

