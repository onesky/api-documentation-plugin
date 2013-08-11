# Item Resources

    GET orders/:id/messages

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

- **messages** — A set of messages in the order.

***

## Errors
None

***

## Example
**Request**

    GET https://api.plugin.onesky.io/1/project/:projectId/orders/:id/messages

**Return** __shortened for example purpose__
``` json
{
    "messages": [
        {
            "id": 123,
            "content": "This is a message",
            "created_at": "2012-03-03 03:03:03 GMT+0",
            "author": {
                "name": "Yusuke T."
            }
        },
        {
            "id": 122,
            "content": "This is a message",
            "created_at": "2012-03-03 03:03:03 GMT+0",
            "author": {
                "name": "OneSky"
            }
        }
    ]
}
```