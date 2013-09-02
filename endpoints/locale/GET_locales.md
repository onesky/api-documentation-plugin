# Locale Resources

    GET locales

## Description
Returns all available locales in the platform.


## Requires authentication
* A valid Developer Key must be provided in `key` parameter.
* A valid Developer Hash must be provided in `dev-hash` parameter.
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
            "id": "en-us",
            "englishName": "English (United States)",
            "localName": "English (United States)",
            "locale": "en",
            "region" : "us"
        },
        {
            "id": "ja-jp",
            "englishName": "Japanese",
            "localName": "日本語",
            "locale": "ja",
            "region" : "jp"
        }
    ]
}
```
