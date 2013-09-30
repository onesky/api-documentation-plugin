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

    GET https://api.plugin.onesky.io/1/projects/:project_id/items/:item_code

**Response**
``` json
{
    "item": {
        "code": "post2",
        "created_at":"2013-03-03T03:03:03+0000",
        "created_at_timestamp":1328475945,
        "translateables": {
            "title": {
                "translations": {
                    "en-US": "How localization help your business (2)?",
                    "zh-TW": "翻譯如何能幫助你的企業（二）？"
                }
            },
            "content": {
                "translations": {
                    "en-US": "This is an attractive title",
                    "zh-TW": "很有趣的題目"
                }
            }
        }
    }
}
```
