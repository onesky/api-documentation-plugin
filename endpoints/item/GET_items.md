# Item Resources

    GET items

## Description
Returns a listing of items in the platform.


## Requires authentication
- Details described [here](/README.md#authentication)


## Parameters
- `locale` _(optional)_ - locale code for the items to display, reference response `code` [here](/endpoints/locale/GET_locales.md#Example) (sample: `en-US`), default base language of the project setting.
- `page` _(optional)_ - page number for pagination, default 1.
- `per_page` _(optional)_ - items to be returned per page, default 15.


## Example
**Request**

    GET https://api.plugin.onesky.io/1/projects/:project_id/items

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
            "created_at": "2013-03-03T03:03:03+0000",
            "created_at_timestamp": 1328475945,
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
