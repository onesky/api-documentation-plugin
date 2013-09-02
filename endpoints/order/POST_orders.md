# Order Resources

    POST orders

## Description
Send an order to professional translators.


## Requires authentication
- A valid Developer Key must be provided in `key` parameter.
- A valid Developer Hash must be provided in `dev-hash` parameter.
- Details described [here](/README.md#authentication)


## Parameters
- **fromLocale** _(required)_ - the locale to be translated from, default base locale of the project
- **toLocales** _(required)_ — locale ids to be translated to, comma separated, refer to [GET locales](/endpoints/locale/GET_locales.md)
- **items** _(required)_ - items to be translated, in [item format](/formats/item.md)


## Example
**Request**

    POST https://api.plugin.onesky.io/1/project/:projectId/orders

**Response**
```
{
    "orders": [
        {
            "id": 123,
            "fromLanguage": "English",
            "fromLocale": "en",
            "toLanguage": "Korean",
            "toLocale": "ko",
            "words": 2013,
            "perWordCost": "0.01",
            "totalCost": "20.13",
            "status": "sent",
            "orderedAt": "2013-01-01T02:02:02+0000",
            "orderedAtTimestamp": 13283746583,
            "completedAt": null,
            "completedAtTimestamp": 0,
            "translator": null
        },
        {
            "id": 123,
            "fromLanguage": "English",
            "fromLocale": "en",
            "toLanguage": "Japanese",
            "toLocale": "ja",
            "words": 2013,
            "perWordCost": "0.01",
            "totalCost": "20.13",
            "status": "sent",
            "orderedAt": "2013-01-01T02:02:02+0000",
            "orderedAtTimestamp": 13283746583,
            "completedAt": null,
            "completedAtTimestamp": 0,
            "translator": null
        }
    ],
    "remainingCredits": "20.12"
}
```
