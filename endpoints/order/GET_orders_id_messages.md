# Item Resources

    GET orders/:id/messages

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

    GET https://api.plugin.onesky.io/1/project/:projectId/orders/:id/messages

**Response**
```
{
    "messages": [
        {
            "id": 123,
            "content": "This is a message",
            "createdAt": "2012-03-03T03:03:03+0000",
            "createdAtTimestamp": 13245678954,
            "author": {
                "name": "Yusuke T."
            }
        },
        {
            "id": 122,
            "content": "This is a message",
            "createdAt": "2012-03-03T03:03:03+0000",
            "createdAtTimestamp": 13245678954,
            "author": {
                "name": "OneSky"
            }
        }
    ]
}
```
