# Quotation Resources

    POST quotations

## Description
Returns a list of quotations.


## Requires authentication
- Details described [here](/README.md#authentication)


## Parameters
- **fromLocale** _(required)_ - the locale to be translated from, default base locale of the project
- **toLocales** _(required)_ - locale ids to be translated to, comma separated e.g. `'en-US,fr-FR,zh-TW'`, refer to [GET locales](/endpoints/locale/GET_locales.md)
- **strings** _(required)_ - strings to be translated, format reference [here](/reference/formats.md#strings)


## Example
**Request**

    POST https://api.plugin.onesky.io/1/project/:project_id/quotations

**Response**
```
{
    "quotations": [
        {
            "id": 123,
            "from_language": "English",
            "from_locale": "en",
            "to_language": "Japanese",
            "to_locale": "jp",
            "words": 2013,
            "per_word_cost": "0.01",
            "total_cost": "20.13",
            "estimated_return_datetime": "2013-01-01T23:00:00+0000",
            "estimated_return_timestamp": 13453435132,
            "estimated_seconds_from_now": 1234567
        },
        {
            "id": 122,
            "from_language": "English",
            "from_locale": "en",
            "to_language": "Korean",
            "to_locale": "ko",
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
