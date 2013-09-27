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

    GET https://api.plugin.onesky.io/1/projects/:project_id/orders

**Response**
``` json
{
    "orders": [
        {
            "id": 123,
            "amount": "695.00",
            "ordered_at": "2013-08-15T08:12:40+0000",
            "ordered_at_timestamp":13283746583,
        },
        {
            "id": 122,
            "amount": "1038.70",
            "ordered_at": "2013-08-15T08:12:40+0000",
            "ordered_at_timestamp":13283746583,
        },
        {
            "id": 121,
            "amount": "337.65",
            "ordered_at": "2013-08-15T08:12:40+0000",
            "ordered_at_timestamp":13283746583,
        }
    ]
}
```
