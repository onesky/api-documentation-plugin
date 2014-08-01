# Order Resources

    GET orders/:order_id/messages

## Description
Returns a listing of orders in the platform.


## Requires authentication
- Details described [here](/README.md#authentication)


## Parameters
- `page` _(optional)_ - page number for pagination, default 1.
- `per_page` _(optional)_ - items to be returned per page, default 15.


## Example
**Request**

    GET https://api.plugin.onesky.io/1/projects/:project_id/orders/:order_id/messages

**Response**
``` json
{
    "messages": [
        {
            "id": 123,
            "content": "This is a message",
            "created_at": "2012-03-03T03:03:03+0000",
            "created_at_timestamp": 13245678954,
            "author": {
                "name": "Yusuke T."
            }
        },
        {
            "id": 122,
            "content": "This is a message",
            "created_at": "2012-03-03T03:03:03+0000",
            "created_at_timestamp": 13245678954,
            "author": {
                "name": "OneSky"
            }
        }
    ]
}
```
