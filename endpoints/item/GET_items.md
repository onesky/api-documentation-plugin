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

    GET https://plugin.api.onesky.io/1/projects/:project_id/items

**Response**
``` json
{
    "items": [
        {
            "id": 2986,
            "code": "post2",
            "created_at": "2013-03-03T03:03:03+0000",
            "created_at_timestamp": 1328475945,
            "language": {
                "code": "en-US",
                "english_name": "English (United States)",
                "local_name": "English (United States)",
                "locale": "en",
                "region" : "US"
            },
            "translateables": {
                "title": "How localization help your business (2)?",
                "content": "This is an attractive title"
            }
        },
        {
            "id": 2985,
            "code": "post1",
            "created_at": "2013-03-03T03:03:03+0000",
            "created_at_timestamp": 1328475945,
            "language": {
                "code": "en-US",
                "english_name": "English (United States)",
                "local_name": "English (United States)",
                "locale": "en",
                "region" : "US"
            },
            "translateables": {
                "title": "How localization help your business (1)?",
                "content": "This is a very attractive title"
            }
        }
    ]
}
```
