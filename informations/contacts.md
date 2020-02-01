# Contacts

{% api-method method="get" host="https://api.wapim.io/" path="api/v1/whatsapp/contacts" %}
{% api-method-summary %}
Get Information of Device
{% endapi-method-summary %}

{% api-method-description %}
This endpoint get contacts.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Succesfully getting contacts.
{% endapi-method-response-example-description %}

```text
[
  {
    "number": "905546452300",
    "pushname": "",
    "name": "Mr. Tarik",
    "group": false
  },
  {
    "number": "90505015342",
    "pushname": "Mr. Mehmet",
    "name": "",
    "group": false
  },
  {
    "number": "905376777564",
    "pushname": "",
    "name": "Mr. Kenan",
    "group": false
  },
  ...
]
```
{% endapi-method-response-example %}
<!---
{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Please read qr code.
{% endapi-method-response-example-description %}

```text
{
   "status":false,
   "code":400,
   "message":"Bad Request",
   "error":{
      "Must be logged in"
   }
}
```
{% endapi-method-response-example %}
-->
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

