# Order Resources

    POST orders

## Description
Send an order to professional translators.


## Requires authentication
- Details described [here](/README.md#authentication)


## Parameters
- `from_locale` _(required)_ - the locale to be translated from, default base locale of the project
- `to_locales` _(required)_ - locale codes to be translated to, comma separated e.g. `'en-US,fr-FR,zh-TW'`, please refer to [GET locales](/endpoints/locale/GET_locales.md)
- `items` _(required)_ - items to be translated, format reference [here](/reference/formats.md#items)
- `tone` _(optional)_ - tone of the translation. `['FORMAL', 'INFORMAL']`, default not specified
- `note` _(optional)_ - note for translator about the order
- `is_including_review` _(optional)_ - set translation review is required. `true` or `false`, default `false`
- `specialization` _(optional)_ - code of project specialization such as `game`, default `general`, please refer to [GET specializations](/endpoints/specialization/GET_specializations.md)


## Example
**Request**

    POST https://plugin.api.onesky.io/1/projects/:project_id/orders

**Response**
```
status 201 Created
```
``` json
{
    "order": {
        "id": 372,
        "amount": "50.00",
        "ordered_at": "2013-08-15T08:12:40+0000",
        "ordered_at_timestamp":13283746583,
        "tasks": [
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
                }
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
                }
            }
        ]
    }
}
```
