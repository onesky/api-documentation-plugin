# Account Resources

    POST sign-in

## Description
Login to [onesky](http://oneskyapp.com) account


## Requires authentication
NONE


## Parameters
- `email` _(required)_ - User email.
- `password` _(required)_ - Account password.


## Example
**Request**

    POST https://api.plugin.onesky.io/1/accounts/sign-in

**Response**
``` json
{
    "accounts":
        [
            {
                "name": "Google",
                "api_key": "188f46c1c3e1dfece67ea4cd20e6043b",
                "api_secret": "ac9fcec178cc235d70d27fce682243b0"
            },
            {
                "name": "Amazon",
                "api_key": "f0163e58fc5c9cda25bbc0a3e0671af7",
                "api_secret": "3e1819d552bf9aa182be04f576a557b2"
            },
            ...
        ]
}
```
