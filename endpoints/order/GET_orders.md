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
- **perpage** _(optional)_ - items to be returned per page, default 15.

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
            "from_language": "English",
            "from_locale": "en",
            "to_language": "Japanese",
            "to_locale": "jp",
            "words": 2013,
            "per_word_cost": "0.01",
            "total_cost": "20.13",
            "status": "in-progress",
            "ordered_at": "2013-01-01 02:02:02 GMT+0",
            "completed_at": null,
            "translator":{
                "name": "Yusuke T."
            }
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
            "status": "completed",
            "ordered_at": "2013-01-01 02:02:02 GMT+0",
            "completed_at": "2013-01-03 02:02:02 GMT+0",
            "translator":{
                "name": "Jinny O."
            }
        }
    ]
}
```