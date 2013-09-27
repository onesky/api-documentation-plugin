# Item Resources

    GET items/:item_id

## Description
Returns the item's attributes.


## Requires authentication
- Details described [here](/README.md#authentication)


## Parameters
None


## Example
**Request**

    GET https://api.plugin.onesky.io/1/projects/:project_id/items/:item_id

**Response**
``` json
{
    "item": {
        "id": "post.101",
        "created_at":"2013-03-03T03:03:03+0000",
        "created_at_timestamp":1328475945,
        "translateables": {
            "title": {
                "name": "title",
                "translations": {
                    "en": "This is very attractive title"
                }
            },
            "content": {
                "name": "content",
                "translations": {
                    "en": "Neque porro quisquam est qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit..."
                }
            }
        }
    }
}
```
