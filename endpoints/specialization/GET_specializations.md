# Specialization Resources

    GET specializations

## Description
List of project specializations. For example, translation of a website about gaming may require longer time than a website about fashion design with similar words count in both sites.


## Requires authentication
* Details described [here](/README.md#authentication)


## Parameters
None


## Example
**Request**

    GET https://api.plugin.onesky.io/1/specializations

**Response**
``` json
{
    "specializations": [
        {
            "code": "general",
            "name": "General Text"
        },
        {
            "code": "game",
            "name": "Gaming"
        },
        ...
    ]
}
```
