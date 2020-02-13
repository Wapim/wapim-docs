---
description: You can send WhatsApp location messages with this endpoint.
---

# Location

{% api-method method="get" host="https://api.wapim.io/api/v1/whatsapp" path="/message/location" %}
{% api-method-summary %}
Send Location
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
phone number
{% endapi-method-parameter %}

{% api-method-parameter name="lat" type="number" required=true %}
lat
{% endapi-method-parameter %}

{% api-method-parameter name="lon" type="number" required=true %}
lon
{% endapi-method-parameter %}

{% api-method-parameter name="title" type="string" required=false %}
title
{% endapi-method-parameter %}

{% api-method-parameter name="scheduled\_time" type="string" required=false %}
schedule time
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{    "name": "Cake's name",    "recipe": "Cake's recipe name",    "cake": "Binary cake"}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```
{    "message": "Ain't no cake like that."}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



