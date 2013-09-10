# Quotation Resources

    POST quotations

## Description
Returns a list of quotations.


## Requires authentication
- Details described [here](/README.md#authentication)


## Parameters
- `from_locale` _(required)_ - the locale to be translated from, default base locale of the project
- `to_locales` _(required)_ - locale ids to be translated to, comma separated e.g. `'en-US,fr-FR,zh-TW'`, refer to [GET locales](/endpoints/locale/GET_locales.md)
- `items` _(required)_ - strings to be translated, format reference [here](/reference/formats.md#items)


## Example
**Request**

    POST https://api.plugin.onesky.io/1/project/:project_id/quotations

**Response**
``` json
{
    "quotations": [
        {
            "id": 123,
            "from": {
                "locale": "en",
                "name": "English",
                "local_name": "English"
            },
            "to": {
                "locale": "ja",
                "name": "Japanese",
                "local_name": "日本語"
            },
            "words": 2013,
            "per_word_cost": "0.01",
            "total_cost": "20.13",
            "estimated_return_datetime": "2013-01-01T23:00:00+0000",
            "estimated_return_timestamp": 13453435132,
            "estimated_seconds_from_now": 1234567
        },
        {
            "id": 122,
            "from": {
                "locale": "en",
                "name": "English",
                "local_name": "English"
            },
            "to": {
                "locale": "ja",
                "name": "Japanese",
                "local_name": "日本語"
            },
            "words": 2013,
            "per_word_cost": "0.01",
            "total_cost": "20.13",
            "estimated_return_datetime": "2013-01-01T23:00:00+0000",
            "estimated_return_timestamp": 13453435132,
            "estimated_seconds_from_now": 1234567
        }
    ]
}
```
