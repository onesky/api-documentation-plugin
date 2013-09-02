# Item Resources

    GET item

## Description
Returns the item's attributes.


## Requires authentication
- A valid Developer Key must be provided in `key` parameter.
- A valid Developer Hash must be provided in `dev-hash` parameter.
- Details described [here](/README.md#authentication)

## Parameters
None


## Example
**Request**

    GET https://api.plugin.onesky.io/1/project/:projectId/items/:id

**Response**
```
{
    "item": {
        "id": "post.101",
        "createdAt":"2013-03-03T03:03:03+0000",
        "createdAtTimestamp":1328475945,
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
