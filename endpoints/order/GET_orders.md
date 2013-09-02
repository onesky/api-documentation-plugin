# Order Resources

    GET orders

## Description
Returns a listing of orders in the platform.


## Requires authentication
- A valid Developer Key must be provided in `key` parameter.
- A valid Developer Hash must be provided in `dev-hash` parameter.
- Details described [here](/README.md#authentication)


## Parameters
- **page** _(optional)_ — page number for pagination, default 1.
- **rpp** _(optional)_ - items to be returned per page, default 15.


## Example
**Request**

    GET https://api.plugin.onesky.io/1/project/:projectId/orders

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
            "status": "in-progress",
            "orderedAt": "2013-08-15T08:12:40+0000",
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
            "orderedAt": "2013-08-15T08:12:40+0000",
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
