# OneSky Plugin API

OneSky Plugin API provides programmatic access to OneSky's translation service.

## Endpoints

#### Account Resources
- [**POST sign-up**](endpoints/account/POST_sign-up.md)
- [**POST sign-in**](endpoints/account/POST_sign-in.md)
- [**GET credit**](endpoints/account/GET_credit.md)


#### Locale Resources
- [**GET locales**](endpoints/locale/GET_locales.md)


#### Specialization Resources
- [**GET specializations**](endpoints/specialization/GET_specializations.md)


#### Project Resources
- [**GET projects**](endpoints/project/GET_projects.md)
- [**POST projects**](endpoints/project/POST_projects.md)


#### Item Resources

- [**GET items**](endpoints/item/GET_items.md)
- [**GET items/:id**](endpoints/item/GET_items_id.md)
- [**DELETE items/:id**](endpoints/item/DELETE_items_id.md)


#### Order Resources
- [**GET orders**](/endpoints/order/GET_orders.md)
- [**GET orders/:id**](/endpoints/order/GET_orders_id.md)
- [**GET orders/:id/items**](endpoints/order/GET_orders_id_items.md)
- [**GET orders/:id/messages**](endpoints/order/GET_orders_id_messages.md)
- [**POST orders**](endpoints/order/POST_orders.md)


#### Quotation Resources
- [**POST quotations**](endpoints/quotation/POST_quotations.md)


## Authentication

All of the endpoints require you to do authentication. You will have to find your own API key and API secret. First login to [oneskyapp](http://www.oneskyapp.com) and find the API key and secret in **Site Settings** under **API Keys & Usage**.

#### Parameters
- string `api_key`
  > Your own API key

- int `timestamp`
  > Current unix timestamp

- string `dev_hash`
  > Calculate with `api_secret` and `timestamp`
  >
  > Formula: `md5(concatenate(<timestamp>, <api_secret>))`

## Request
We accept request data in JSON format. Please specify request header with `Content-Type: application/json; charset=utf-8` and encode the data in JSON format.

SSL is applied to protect all request data. Make sure you are using https to initiate request.

## Response
Successful request will response with either `200` or `201` status code togehter with response data if there is. When there is a new record created, `201 Created` will be used. Otherwise, `200 OK` will apply.

Failure request will response with an error status code together with an error message:
``` json
{ "code": 400, "message": "Your request cannot be processed" }
```

Currently, we only support JSON data format encoded in UTF-8 charset in response.
