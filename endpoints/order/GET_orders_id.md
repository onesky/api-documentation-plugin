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

<<<<<<< HEAD
    GET https://plugin.api.onesky.io/1/projects/:project_id/orders/:order_id
=======
    GET https://api.plugin.onesky.io/1/projects/:project_id/orders/:order_id
>>>>>>> 1936fca727ae8b9114793808a87c9a161f6cbf5b

**Response**
``` json
{
    "orders": [
        {
            "id": 123,
            "amount": "695.00",
            "ordered_at": "2013-08-15T08:12:40+0000",
            "ordered_at_timestamp":13283746583,
            "tasks": [
                {
                    "id": 355,
                    "status": "completed",
                    "completed_at": 2013-08-17T15:35:37+0000,
                    "completed_at_timestamp": 1376753737,
                    "translator":{
                        "name": "Jinny O."
                    },
                    "from_language": {
                        "code": "en-US",
                        "english_name": "English (United States)",
                        "local_name": "English (United States)",
                        "locale": "en",
                        "region" : "US"
                    },
                    "to_language": {
                        "code": "ja-JP",
                        "english_name": "Japanese",
                        "local_name": "日本語",
                        "locale": "ja",
                        "region" : "JP"
                    }
                },
                {
                    "id": 356,
                    "status": "completed",
                    "completed_at": 2013-08-17T13:05:20+0000,
                    "completed_at_timestamp": 1376744720,
                    "translator":{
                        "name": "Jinny O."
                    },
                    "from_language": {
                        "code": "en-US",
                        "english_name": "English (United States)",
                        "local_name": "English (United States)",
                        "locale": "en",
                        "region" : "US"
                    },
                    "to_language": {
                        "code": "ko-KR",
                        "english_name": "Korean",
                        "local_name": "한국어",
                        "locale": "ko",
                        "region" : "KR"
                    }
                }
            ]
        }
    ]
}
```
