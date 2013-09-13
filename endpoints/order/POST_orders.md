# Order Resources

    POST orders

## Description
Send an order to professional translators.


## Requires authentication
- Details described [here](/README.md#authentication)


## Parameters
- `from_locale` _(required)_ - the locale to be translated from, default base locale of the project
- `to_locales` _(required)_ - locale codes to be translated to, comma separated e.g. `'en-US,fr-FR,zh-TW'`, refer to [GET locales](/endpoints/locale/GET_locales.md)
- `items` _(required)_ - items to be translated, format reference [here](/reference/formats.md#items)
- `tone` _(optional)_ - tone of the translation. `FORMAL`, `INFORMAL`, default not specified
- `note` _(optional)_ - note for translator about the order
- `is_including_review` _(optional)_ - if need to add extra reviewer. `1` or `0`, default `0`

## Example
**Request**

    POST https://api.plugin.onesky.io/1/project/:project_id/orders

**Response**
```
status 201 Created
```
