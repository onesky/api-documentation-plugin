# Item Resources

    GET orders

## Description
Returns a listing of orders in the platform.

***

## Requires authentication
* A valid Developer Key must be provided in `key` parameter.
* A valid Developer Hash must be provided in `dev-hash` parameter.

***

## Parameters
- **page** _(optional)_ — page number for pagination, default 1.
- **rpp** _(optional)_ - items to be returned per page, default 15.

***

## Return format
An array with the following keys and values:

- **orders** — A set of orders made.

***

## Errors
None

***

## Example
**Request**

    GET https://api.plugin.onesky.io/1/project/:projectId/orders

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
            "status": "in-progress",
            "orderedAt": "2013-08-15T08:12:40Z", // ISO String 
            "orderedAtTimestamp":13283746583,
            "completedAt": null,
            "completedAtTimestamp": 0,
            "translator":{
                "name": "Yusuke T."
            }
       },
        {
            "id": 122,
            "fromLanguage": "English",
            "fromLocale": "en",
            "toLanguage": "Japanese",
            "toLocale": "jp",
            "words": 2013,
            "perWordCost": "0.01",
            "totalCost": "20.13",
            "status": "completed",
            "orderedAt": "2013-08-15T08:12:40Z",
            "orderedAtTimestamp":13283746583,
            "completedAt": null,
            "completedAtTimestamp": 0,
            "translator":{
                "name": "Jinny O."
            }
        }
    ]
}
```
