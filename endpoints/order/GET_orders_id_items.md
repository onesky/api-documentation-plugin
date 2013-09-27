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

    GET https://plugin.api.onesky.io/1/projects/:project_id/orders/:order_id/items

**Response**
``` json
{
    "items": [
        {
            "id": "post2",
            "created_at": "2013-03-03T03:03:03+0000",
            "created_at_timestamp": 1328475945,
            "translateables": [
                "title": {
                    "name": "title",
                    "translations": [
                        {
                            "en-US": "design glasses",
                            "zh-TW": "設計眼鏡",
                            "ja-JP": "メガネのデザイン"
                        },
                        ...
                    ]
                }
            ]
        },
        {
            "id": "post1",
            "created_at": "2013-03-03T03:03:03+0000",
            "created_at_timestamp": 1328475945,
            "translateables": [
                "content": {
                    "name": "content",
                    "translations": [
                        {
                            "en-US": "design glasses description",
                            "zh-TW": "設計的眼鏡描述",
                            "ja-JP": "デザインのガラスの説明"
                        },
                        ...
                    ]
                }
            ]
        }
    ]
}
```
