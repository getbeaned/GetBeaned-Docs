---
description: Work in progress
---

# The GetBeaned API

{% swagger baseUrl="https://getbeaned.api-d.com" path="/api/users/" method="post" summary="Add an user" %}
{% swagger-description %}
This endpoint allows you to upload an user data to the website. This is a required step to be able to add actions.

\




\


The endpoint will update or create the user automatically.
{% endswagger-description %}

{% swagger-parameter in="header" name="Update" type="boolean" %}
False if we don't want to update the user because the data is stale
{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authentication" type="string" %}
Authentication token supplied on request.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="discord_default_avatar_url" type="string" %}
Default Discord CDN URL for the user avatar.
{% endswagger-parameter %}

{% swagger-parameter in="body" name="discord_avatar_url" type="string" %}
Discord CDN URL to the PNG (static) or WEBP (animated) avatar of the user
{% endswagger-parameter %}

{% swagger-parameter in="body" name="discord_discriminator" type="integer" %}
The user Discriminator (Excluding the 

`#`

)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="discord_name" type="string" %}
Name of the user
{% endswagger-parameter %}

{% swagger-parameter in="body" name="discord_id" type="boolean" %}
Discord user ID
{% endswagger-parameter %}

{% swagger-parameter in="body" name="discord_bot" type="boolean" %}
Please set that to True if the user is a bot
{% endswagger-parameter %}

{% swagger-response status="200" description="Cake successfully retrieved." %}
```javascript
{
 'status': 'ok',
 'message': 'User existed in database already',
 'result': '[User representation]'
 }
```
{% endswagger-response %}

{% swagger-response status="302" description="Error when saving the new user" %}
```javascript
{
    'status': 'error',
    'errors': ['List of errors']
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="https://getbeaned.api-d.com" path="/api/users/<int:guild_id>/<int:user_id>/counters/" method="get" summary="API Users Counter" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="" type="string" %}

{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
```
{% endswagger-response %}
{% endswagger %}
