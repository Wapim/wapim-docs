# -Videos

{% api-method method="post" host="https://api.cakes.com" path="/api/v1/whatsapp/message/video" %}
{% api-method-summary %}
Send Video Message
{% endapi-method-summary %}

{% api-method-description %}
You can send video message with this endpoint.
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

{% api-method-parameter name="scheduled\_time" type="string" required=false %}
Schedule time \(Timestamp\)
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```text
{    "name": "Cake's name",    "recipe": "Cake's recipe name",    "cake": "Binary cake"}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```text
{    "message": "Ain't no cake like that."}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

