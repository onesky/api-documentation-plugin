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
            "name": "Sportswear",
            "platform": "Magento",
            "base_language": {
                "code": "en-US",
                "english_name": "English (United States)",
                "local_name": "English (United States)",
                "locale": "en",
                "region" : "US"
            }
        },
        {
            "id": 8357,
            "name": "Jeans",
            "platform": "Magento",
            "base_language": {
                "code": "ja-JP",
                "english_name": "Japanese",
                "local_name": "日本語",
                "locale": "ja",
                "region" : "JP"
            }
        },
        ...
    ]
}
```
