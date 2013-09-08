# Locale Resources

    GET locales

## Description
Returns all available locales in the platform.


## Requires authentication
* Details described [here](/README.md#authentication)


## Parameters
None


## Example
**Request**

    GET https://api.plugin.onesky.io/1/locales

**Response**
```
{
    "locales": [
        {
            "code": "en-US",
            "english_name": "English (United States)",
            "local_name": "English (United States)",
            "locale": "en",
            "region" : "US"
        },
        {
            "code": "ja-JP",
            "english_name": "Japanese",
            "local_name": "日本語",
            "locale": "ja",
            "region" : "JP"
        }
    ]
}
```
