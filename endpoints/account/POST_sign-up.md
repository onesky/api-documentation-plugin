# Account Resources

    POST sign-up

## Description
Register account in [onesky](http://oneskyapp.com)


## Requires authentication
NONE


## Parameters
- `email` _(required)_ - User email to register account.
- `platform` _(required)_ - Platform of plugin such as `magento`, `wordpress`
- `locale` _(required)_ - Base language used by the project. i.e. `en-US`, `zh-TW`


## Example
**Request**

    POST https://api.plugin.onesky.io/1/sign-up

**Response**
```
status 201 Created
```
