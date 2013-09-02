# Item Resources

    DELETE item

## Description
Returns the item's attributes.


## Requires authentication
- A valid Developer Key must be provided in `key` parameter.
- A valid Developer Hash must be provided in `dev-hash` parameter.
- Details described [here](/README.md#authenticaion)


## Parameters
None


## Example
**Request**

    DELETE https://api.plugin.onesky.io/1/project/:projectId/items/:id

**Response**
```
status 200 OK
```
