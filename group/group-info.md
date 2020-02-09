# Group Information

{% api-method method="post" host="https://api.wapim.io/" path="api/v1/whatsapp/group/info" %}
{% api-method-summary %}
Get Group Information
{% endapi-method-summary %}

{% api-method-description %}
This endpoint get contacts.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="gid" type="string" required=true %}
Group ID
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Succesfully getting info of groups.
{% endapi-method-response-example-description %}

```text
{
    "status": true,
    "code": 200,
    "message": {
        "jid": "",
        "owner": "905320602911@c.us",
        "subject": "Wapim.io",
        "subjectTime": 1560716540,
        "subjectOwner": "905320602911",
        "desc": "",
        "descId": "",
        "descTime": 0,
        "descOwner": "",
        "creation": 1560716540,
        "status": 0,
        "participants": [
            {
                "id": "905320602911",
                "isAdmin": false,
                "isSuperAdmin": false
            },
            {
                "id": "905348372911",
                "isAdmin": true,
                "isSuperAdmin": false
            },
            {
                "id": "905303001965",
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

