# Order Resources

    GET orders

## Description
Returns a listing of orders in the platform.


## Requires authentication
- Details described [here](/README.md#authentication)


## Parameters
- `page` _(optional)_ - page number for pagination, default 1.
- `per_page` _(optional)_ - items to be returned per page, default 15.


## Example
**Request**

    GET https://api.plugin.onesky.io/1/project/:project_id/orders

**Response**
``` json
{
    "orders": [
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
            "status": "in-progress",
            "ordered_at": "2013-08-15T08:12:40+0000",
            "ordered_at_timestamp":13283746583,
            "completed_at": null,
            "completed_at_timestamp": 0,
            "translator":{
                "name": "Yusuke T."
            }
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
            "status": "completed",
            "ordered_at": "2013-08-15T08:12:40+0000",
            "ordered_at_timestamp":13283746583,
            "completed_at": null,
            "completed_at_timestamp": 0,
            "translator":{
                "name": "Jinny O."
            }
        }
    ]
}
```
