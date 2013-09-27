# Order Resources

    GET orders/:order_id/items

## Description
Return details of an order


## Requires authentication
- Details described [here](/README.md#authentication)


## Parameters
NONE


## Example
**Request**

    GET https://api.plugin.onesky.io/1/projects/:project_id/orders/:order_id/items

**Response**
``` json
{
    "items": [
        {
            "id": "post.101",
            "created_at": "2013-03-03T03:03:03+0000",
            "created_at_timestamp": 1328475945,
            "translateables": {
                "title": {
                    "name": "title",
                    "translations": [
                        {
                            "en": "This is very attractive title"
                        },
                        ...
                    ]
                },
                "content": {
                    "name": "content",
                    "translations": [
                        {
                        "en": "Neque porro quisquam est qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit..."
                        },
                        ...
                    ]
                }
            }
        },
        {
            "id": "post.100",
            "created_at": "2013-03-03T03:03:03+0000",
            "created_at_timestamp": 1328475945,
            "translateables": {
                "title": {
                    "name": "title",
                    "translations": [
                        {
                            "en": "This is very attractive title"
                        },
                        ...
                    ]
                },
                "content": {
                    "name": "content",
                    "translations": [
                        {
                        "en": "Neque porro quisquam est qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit..."
                        },
                        ...
                    ]
                }
            }
        }
    ]
}
```
