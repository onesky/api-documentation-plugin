# Item Resources

    GET locales

## Description
Returns a listing of locales in the platform.

***

## Requires authentication
* A valid Developer Key must be provided in `key` parameter.
* A valid Developer Hash must be provided in `dev-hash` parameter.

***

## Parameters
None

***

## Return format
An array with the following keys and values:

- **locales** — A set of locales available.

***

## Errors
None

***

## Example
**Request**

    GET https://api.plugin.onesky.io/1/locales

**Return** __shortened for example purpose__
``` json
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