# Project Resources

    POST projects

## Description
Create project of specified platform


## Requires authentication
* Details described [here](/README.md#authentication)


## Parameters
- `platform` _(required)_ - Platform of projects. Currently, only support `magento`
- `name` _(required)_ - Name of the project such as `Glasses`
- `locale` _(required)_ - Base language of the project such as `en-US`, refer to [GET locales](/endpoints/locale/GET_locales.md)


## Example
**Request**

    POST https://api.plugin.onesky.io/1/projects

**Response**
``` json
{
    "project":
        {
            "id": 8777,
            "name": "Glasses",
            "platform": "Magento",
            "base_language": {
                "code": "ja-JP",
                "english_name": "Japanese",
                "local_name": "日本語",
                "locale": "ja",
                "region" : "JP"
            }
        }
}
```
