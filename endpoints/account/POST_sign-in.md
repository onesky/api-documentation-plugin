# Account Resources

    POST sign-in

## Description
Login to [onesky](http://oneskyapp.com) account


## Requires authentication
NONE


## Parameters
- `email` _(required)_ - User email.
- `password` _(required)_ - Account password.
- `platform` _(required)_ - Platform of plugin such as `magento`.

> For `platform`, currently we only support `magento`.


## Example
**Request**

    POST https://api.plugin.onesky.io/1/sign-in

**Response**
``` json
{
    "api_key": "oieu3vt98y45b98y4n5ft9w89fRT6yeb",
    "api_secret": "9w458ynpwo5iunttfytwfpvevtERVTYw",
    "projects":
        [
            {
                "name": "Magento",
                "platform_id": 6835
            },
            {
                "name": "Magento 2",
                "platform_id": 6836
            },
            ...
        ]
}
```
