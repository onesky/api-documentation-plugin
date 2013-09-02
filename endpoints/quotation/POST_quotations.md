# Quotation Resources

    POST quotations

## Description
Returns a list of quotations.


## Requires authentication
- A valid Developer Key must be provided in `key` parameter.
- A valid Developer Hash must be provided in `dev-hash` parameter.
- Details described [here](/README.md#authentication)


## Parameters
- **fromLocale** _(required)_ - the locale to be translated from, default base locale of the project
- **toLocales** _(required)_ - locale ids to be translated to, comma separated e.g. `'en-US,fr-FR,zh-TW'`, refer to [GET locales](/endpoints/locale/GET_locales.md)
- **strings** _(required)_ - strings to be translated, format reference [here](/reference/formats.md#strings)


## Example
**Request**

    POST https://api.plugin.onesky.io/1/project/:projectId/quotations

**Response**
```
{
    "quotations": [
        {
            "id": 123,
            "fromLanguage": "English",
            "fromLocale": "en",
            "toLanguage": "Japanese",
            "toLocale": "jp",
            "words": 2013,
            "perWordCost": "0.01",
            "totalCost": "20.13",
            "estimatedReturnDatetime": "2013-01-01T23:00:00+0000",
            "estimatedReturnTimestamp": 13453435132,
            "estimatedSecondsFromNow": 1234567
        },
        {
            "id": 122,
            "fromLanguage": "English",
            "fromLocale": "en",
            "toLanguage": "Korean",
            "toLocale": "ko",
            "words": 2013,
            "perWordCost": "0.01",
            "totalCost": "20.13",
            "estimatedReturnDatetime": "2013-01-01T23:00:00+0000",
            "estimatedReturnTimestamp": 13453435132,
            "estimatedSecondsFromNow": 1234567
        }
    ]
}
```
