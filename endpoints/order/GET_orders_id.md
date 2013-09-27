# Order Resources

    GET orders/:order_id

## Description
Return details of an order


## Requires authentication
- Details described [here](/README.md#authentication)


## Parameters
NONE


## Example
**Request**

    GET https://api.plugin.onesky.io/1/projects/:project_id/orders/:order_id

**Response**
``` json
{
    "order": {
        "id": 123,
        "from_language": {
            "code": "en-US",
            "english_name": "English (United States)",
            "local_name": "English (United States)",
            "locale": "en",
            "region" : "US"
        },
        "to_languages": {
            "code": "ko-KR",
            "english_name": "Korean",
            "local_name": "한국어",
            "locale": "ko",
            "region" : "KR"
        },
        "status": "in-progress",
        "ordered_at": "2013-08-15T08:12:40+0000",
        "ordered_at_timestamp":13283746583,
        "completed_at": null,
        "completed_at_timestamp": 0,
        "translator":{
            "name": "Yusuke T."
        },
        "items": [
            {
                "product_name": "iPhone 5s",
                "description": "First iPhone with touch ID"
            },
            {
                "product_name": "iPhone 5c",
                "description": "Colourful iPhone"
            }
        ]
    }
}
```
