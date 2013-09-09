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

    POST https://api.plugin.onesky.io/1/sign-in

**Response**
```
{
    "api_key": "oieu3vt98y45b98y4n5ft9w89fRT6yeb",
    "api_secret": "9w458ynpwo5iunttfytwfpvevtERVTYw",
    "project_id": 6385
}
```
