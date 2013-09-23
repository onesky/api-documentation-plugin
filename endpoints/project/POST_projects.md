# Project Resources

    POST projects

## Description
Create project of specified platform


## Requires authentication
* Details described [here](/README.md#authentication)


## Parameters
- `platform` _(required)_ - Platform of projects. Currently, only support `magento`
- `name` _(required)_ - Name of the project such as `Glasses`


## Example
**Request**

    POST https://api.plugin.onesky.io/1/projects

**Response**
``` json
{
    "project":
        {
            "id": 8777,
            "name": "Glasses"
        }
}
```
