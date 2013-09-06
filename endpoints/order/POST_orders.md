# Order Resources

    POST orders

## Description
Send an order to professional translators.


## Requires authentication
- Details described [here](/README.md#authentication)


## Parameters
- `fromLocale` _(required)_ - the locale to be translated from, default base locale of the project
- `toLocales` _(required)_ - locale codes to be translated to, comma separated e.g. `'en-US,fr-FR,zh-TW'`, refer to [GET locales](/endpoints/locale/GET_locales.md)
- `items` _(required)_ - items to be translated, format reference [here](/reference/formats.md#items)


## Example
**Request**

    POST https://api.plugin.onesky.io/1/project/:project_id/orders

**Response**
```
{
    "orders": [
        {
            "id": 123,
            "from_language": "English",
            "from_locale": "en",
            "to_language": "Korean",
            "to_locale": "ko",
            "words": 2013,
            "per_word_cost": "0.01",
            "total_cost": "20.13",
            "status": "sent",
            "ordered_at": "2013-01-01T02:02:02+0000",
            "ordered_at_timestamp": 13283746583,
            "completed_at": null,
            "completed_at_timestamp": 0,
            "translator": null
        },
        {
            "id": 123,
            "from_tanguage": "English",
            "from_tocale": "en",
            "to_tanguage": "Japanese",
            "to_tocale": "ja",
            "words": 2013,
            "per_word_cost": "0.01",
            "total_cost": "20.13",
            "status": "sent",
            "ordered_at": "2013-01-01T02:02:02+0000",
            "ordered_at_timestamp": 13283746583,
            "completed_at": null,
            "completed_at_timestamp": 0,
            "translator": null
        }
    ],
    "remainingCredits": "20.12"
}
```
