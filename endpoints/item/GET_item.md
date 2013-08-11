# Item Resources

    GET item

## Description
Returns the item's attributes.

***

## Requires authentication
* A valid Developer Key must be provided in `key` parameter.
* A valid Developer Hash must be provided in `dev-hash` parameter.

***

## Parameters
- **project** _(required)_ — project id storing the items.
- **id** _(required)_ - item id

***

## Return format
An array with the following keys and values:

- **item** — A set of items available.

***

## Errors
None

***

## Example
**Request**

    GET https://api.plugin.onesky.io/1/items

**Return** __shortened for example purpose__
``` json
{
    "item": {
        "id": "post.101",
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
