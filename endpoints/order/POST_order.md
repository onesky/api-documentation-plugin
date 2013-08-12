# Order Resources

    POST orders

## Description
Send an order to professional translators.

***

## Requires authentication
* A valid Developer Key must be provided in `key` parameter.
* A valid Developer Hash must be provided in `dev-hash` parameter.

***

## Parameters
- **fromLocale** _(required)_ - the locale to be translated from, default base locale of the project
- **toLocales** _(required)_ — locale ids to be translated to, comma separated, refer to [GET locales](https://github.com/onesky/api-documentation-plugin/blob/master/endpoints/locale/GET_locales.md)
- **items** _(required)_ - items to be translated, in [item format](https://github.com/onesky/api-documentation-plugin/blob/master/formats/item.md)

***

## Return format
An array with the following keys and values:

- **orders** — A set of orders made.
- **remainingCredits** - Amount of credits remaining.

***

## Errors
None

***

## Example
**Request**

    POST https://api.plugin.onesky.io/1/project/:projectId/orders

**Return** __shortened for example purpose__
``` json
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
            "orderedAt": "2013-01-01 02:02:02 GMT+0",
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
            "orderedAt": "2013-01-01 02:02:02 GMT+0",
            "orderedAtTimestamp": 13283746583,
            "completedAt": null,
            "completedAtTimestamp": 0,
            "translator": null
        }
    ],
    "remainingCredits": "20.12"
}
```