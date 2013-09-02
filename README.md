# OneSky Plugin API

OneSky Plugin API provides programmatic access to OneSky's translation service.

***

## Endpoints

#### Locale Resources
- **[<code>GET</code> locales](https://github.com/onesky/api-documentation-plugin/blob/master/endpoints/locale/GET_locales.md)**


#### Item Resources

- **[<code>GET</code> items](https://github.com/onesky/api-documentation-plugin/blob/master/endpoints/item/GET_items.md)**
- **[<code>GET</code> items/:id](https://github.com/onesky/api-documentation-plugin/blob/master/endpoints/item/GET_items_id.md)**
- **[<code>DELETE</code> items/:id](https://github.com/onesky/api-documentation-plugin/blob/master/endpoints/item/DELETE_items_id.md)**


#### Order Resources
- **[<code>GET</code> orders](https://github.com/onesky/api-documentation-plugin/blob/master/endpoints/order/GET_orders.md)**
- **[<code>GET</code> orders/:id/messages](https://github.com/onesky/api-documentation-plugin/blob/master/endpoints/order/GET_orders_id_messages.md)**
- **[<code>POST</code> orders](https://github.com/onesky/api-documentation-plugin/blob/master/endpoints/order/POST_orders.md)**


#### Quotation Resources
- **[<code>POST</code> quotations](https://github.com/onesky/api-documentation-plugin/blob/master/endpoints/quotation/POST_quotations.md)**


## Authentication

All of the endpoints require you to do authentication. You will have to find your own api-key and api-secret. First login to [oneskyapp](http://www.oneksyapp.com) and find the API key and secret in **Site Settings** under **API Keys & Usage**.

#### Parameters
- string `api-key`
  > Your own API key

- int `timestamp`
  > Current unix timestamp

- string `dev-hash`
  > Calculate with `api-secret` and `timestamp`
  >
  > Formula: `md5(concatenate(<timestamp>, <api-secret>))`

## Request
We accept request data in JSON format. Please specify request header with `content-type: application/json` and format the data in JSON.

## Response
Successful request will response with either `200` or `201` status code togehter with response data if there is. When there is a new record created, `201 Created` will be used. Otherwise, `200 OK` will apply.

Failure request will response with an error status code together with an error message:
```
{'code': 400, 'message': 'Your request cannot be processed'}
```

Currently, we only support JSON data format in response.
