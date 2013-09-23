# Order Resources

    POST orders

## Description
Send an order to professional translators.


## Requires authentication
- Details described [here](/README.md#authentication)


## Parameters
- `from_locale` _(required)_ - the locale to be translated from, default base locale of the project
- `to_locales` _(required)_ - locale codes to be translated to, comma separated e.g. `'en-US,fr-FR,zh-TW'`, refer to [GET locales](/endpoints/locale/GET_locales.md)
- `items` _(required)_ - items to be translated, format reference [here](/reference/formats.md#items)
- `tone` _(optional)_ - tone of the translation. `['FORMAL', 'INFORMAL']`, default not specified
- `note` _(optional)_ - note for translator about the order
- `is_including_review` _(optional)_ - set translation review is required. `true` or `false`, default `false`


## Example
**Request**

    POST https://api.plugin.onesky.io/1/project/:project_id/orders

**Response**
```
status 201 Created
```
``` json
{
    "amount": "50.00"
    "orders": [
        {
            "id": 123,
            "from_language": {
                "code": "en-US",
                "english_name": "English (United States)",
                "local_name": "English (United States)",
                "locale": "en",
                "region" : "US"
            },
            "to_language": {
                "code": "ja-JP",
                "english_name": "Japanese",
                "local_name": "日本語",
                "locale": "ja",
                "region" : "JP"
            },
            "ordered_at": "2013-08-15T08:12:40+0000",
            "ordered_at_timestamp":13283746583,
        },
        {
            "id": 122,
            "from_language": {
                "code": "en-US",
                "english_name": "English (United States)",
                "local_name": "English (United States)",
                "locale": "en",
                "region" : "US"
            },
            "to_language": {
                "code": "ko-KR",
                "english_name": "Korean",
                "local_name": "한국어",
                "locale": "ko",
                "region" : "KR"
            },
            "ordered_at": "2013-08-15T08:12:40+0000",
            "ordered_at_timestamp":13283746583,
        }
    ]
}
```
