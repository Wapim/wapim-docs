# Generate QR Code

{% api-method method="get" host="https://api.wapim.io/api/v1/whatsapp" path="/login" %}
{% api-method-summary %}
Generate QR Code
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

{% endapi-method-response-example-description %}

```text
{
	"status": true,
	"code": 200,
	"message": "Success",
	"data": {
		"qrcode": "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAQAAAAEAAQMAAABmvDolAAAABlBMVEX///8AAABVwtN+AAACqElEQVR42uyZzY3rMAyEx/BBR5agTqzGgthGGpM7UQk66iBoHkjtbn5eAZaB6Gh8h9AeDYcMvud7LngcSUYAKyvmVEG6iEmf5gsBCXBHDtxw84qUUPQBMI8E6M+WJrs+o1ZRFkx55WMw4LD3evMkk77oMiIQJQJCVsA7uuaOywEmmCnf5cFNH/QyPxV1LqCX7MiL7PnmH6l6F8uiH+ftbp4M9CO0ClbOVFW7+Ol15wJahSMbIBUzZwIlUG/ibSAglYApQ5psmBM8gmtYZMOVAHgXGbH0FkESAcACDAXAxRLyIuZzYCpw7V1R5wOOJbjjRyEz7epNrxdvBMBcK+QeD26oqunommyyXQnwACP0Om6+ov5a8fTbLwYBQgGmPGX9EnOiAibycQCXCsisDqEuxwQUBda8jgOo8xZIw0qm30zrIu5PwQwAeBd/kxjgLYkFHvzrF1cBWPQJ85y0MQNFrfgudRzAXE5b86QhpwP6cZj/ktgIgFURfzqvCsZ87f7sF+cD+mat89rVS6oHK0qN9zqAs8igXY/9SzC6o0B2bgMBqQSbcbpg5oTw0bsHACzkTGw/2dzKUpfDa2s+G9BBzKacNZuJ0XpceC1zAIDFXEt2NbFUfd8e8JnMLwEkkk2i7Kxe84OOk9AMPBKg3jux4S609KBlWWuuAwHJ0TU5uAlZPRMCFm1qf6IfAlAh55A11azURqyKkPas4hKAjpPCPNkuSQWDRaGnos4H7KjLNXkk6PhAd/AtcJ4P9G0SbRHHrQ88izvy/W0lfjaQLNNAdkMAtWIXX+eLEQDSHXmypL124EMw1wEWE8yabE9rWez1bg4D7CQfrL4EixP7f1WcCtgyeZFNNtvbM+rLtv8axgH61es7rpvvGzCb1G8XAr7ne4Y6/wIAAP//Bn4lWQdX5lMAAAAASUVORK5CYII=",
		"timeout": 20
	},
	"logged_in": false
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
	.get('https://api.wapim.io/api/v1/whatsapp/login', {
		headers: {
			token: 'YOUR_WAPIM_TOKEN',
		},
	})
	.then(response => console.log(response.data))
	.catch(error => console.log(error.response.data));

```
{% endtab %}

{% tab title="cURL" %}
```

```
{% endtab %}
{% endtabs %}

