# Order Resources

    POST orders

## Description
Send an order to professional translators.


## Requires authentication
- Details described [here](/README.md#authentication)


## Parameters
- `fromLocale` _(required)_ - the locale to be translated from, default base locale of the project
- `toLocales` _(required)_ - locale codes to be translated to, comma separated e.g. `'en-US,fr-FR,zh-TW'`, refer to [GET locales](/endpoints/locale/GET_locales.md)
- `items` _(required)_ - items to be translated, format reference [here](/reference/formats.md#items)


## Example
**Request**

    POST https://api.plugin.onesky.io/1/project/:project_id/orders

**Response**
```
status 201 Created
```
