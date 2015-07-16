# Language Pair Resources

    GET language-pairs

## Description
Returns order supported language pairs


## Requires authentication
* Details described [here](/README.md#authentication)


## Parameters
- `from_locale` _(required)_ - locale code of language from, reference response `code` [here](/endpoints/locale/GET_locales.md#Example) (sample: `en-US`)


## Example
**Request**

    GET https://plugin.api.onesky.io/1/language-pairs

**Response**
``` json
{
    "meta": {
        "status": 200,
        "record_count": 451
    },    
    "data": [
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
        },
        ...
    ]
}
```
