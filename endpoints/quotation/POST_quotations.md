# Item Resources

    POST quotations

## Description
Returns a list of quotations.

***

## Requires authentication
* A valid Developer Key must be provided in `key` parameter.
* A valid Developer Hash must be provided in `dev-hash` parameter.

***

## Parameters
- **from_locale** _(required)_ - the locale to be translated from, default base locale of the project
- **locales** _(required)_ — locales to be translated to
- **strings** _(required)_ - strings to be translated, simply an array

***

## Return format
An array with the following keys and values:

- **quotations** — A set of quotations available.

***

## Errors
None

***

## Example
**Request**

    POST https://api.plugin.onesky.io/1/project/:id/quotations

**Return** __shortened for example purpose__
``` json
{
    "quotations": [
        {
            "id": 123,
            "from_language": "English",
            "from_locale": "en",
            "to_language": "Japanese",
            "to_locale": "jp",
            "words": 2013,
            "per_word_cost": "0.01",
            "total_cost": "20.13",
            "estimated_return_time": "2013-01-01 23:00:00 GMT+0",
            "estimated_seconds_from_now": 1234567
        },
        {
            "id": 124,
            "from_language": "English",
            "from_locale": "en",
            "to_language": "Korean",
            "to_locale": "ko",
            "words": 2013,
            "per_word_cost": "0.01",
            "total_cost": "20.13",
            "estimated_return_time": "2013-01-01 23:00:00 GMT+0",
            "estimated_seconds_from_now": 1234567
        }
    ]
}
```