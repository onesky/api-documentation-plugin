# Item Resources

    DELETE item

## Description
Returns the item's attributes.

***

## Requires authentication
* A valid Developer Key must be provided in `key` parameter.
* A valid Developer Hash must be provided in `dev-hash` parameter.

***

## Parameters
None

***

## Return format
A JSON object containing keys: status, message and error(if happened).

***

## Errors
None

***

## Example
**Request**

    DELETE https://api.plugin.onesky.io/1/project/:projectId/items/:id

**Return** __shortened for example purpose__
``` json
{
    "status": 200,
    "message": "Successfully deleted an item.",
    "error": "None"
}
```
