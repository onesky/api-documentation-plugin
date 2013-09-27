# Project Resources

    GET projects

## Description
Retrieve all projects of specified platform


## Requires authentication
* Details described [here](/README.md#authentication)


## Parameters
- `platform` _(required)_ - Platform of projects. Currently, only support `magento`


## Example
**Request**

    GET https://plugin.api.onesky.io/1/projects

**Response**
``` json
{
    "projects": [
        {
            "id": 8356,
            "name": "Sportswear"
        },
        {
            "id": 8357,
            "name": "Jeans"
        },
        ...
    ]
}
```
