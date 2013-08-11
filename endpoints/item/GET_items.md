# Item Resources

    GET items

## Description
Returns a listing of items in the platform.

***

## Requires authentication
* A valid Developer Key must be provided in `key` parameter.
* A valid Developer Hash must be provided in `dev-hash` parameter.

***

## Parameters
- **locale** _(optional)_ — locale for the items to display, default base language of the project setting.
- **page** _(optional)_ — page number for pagination, default 1.
- **rpp** _(optional)_ - items to be returned per page, default 15.

***

## Return format
An array with the following keys and values:

- **items** — A set of items available.

***

## Errors
None

***

## Example
**Request**

    GET https://api.plugin.onesky.io/1/project/:projectId/items

**Return** __shortened for example purpose__
``` json
{
    "items": [
        {
            "id": "post.101",
            "createdAt": "2013-03-03 03:03:03 GMT+0",
            "createdAtTimestamp": 1328475945,
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
        },
        {
            "id": "post.100",
            "createdAt": "2013-03-03 03:03:03 GMT+0",
            "createdAtTimestamp": 1328475945,
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
    ]
}
```