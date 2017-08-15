# 

TODO: Add a description



## Base URL

The Base URL for this API is `http://www.example.com`



## Authentication
The type of authentication used by this API is: `OAuth v2 Bearer Token / Personal Access Token`



# <a name="api_reference"></a>API Reference

* [Brands](#brands)
* [Customers](#customers)
* [Customer Groups](#customer_groups)
* [Consignments](#consignments)
* [Inventory](#inventory)
* [Outlets](#outlets)
* [Price Books](#price_books)
* [Price Book Products](#price_book_products)
* [Products](#products)
* [Product Images](#product_images)
* [Product Types](#product_types)
* [Registers](#registers)
* [Tags](#tags)
* [Sales](#sales)
* [Suppliers](#suppliers)

## <a name="brands"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Brands") Brands


### <a name="list_brands"></a>![Endpoint: ](https://apidocs.io/img/method.png "List brands") List brands


**`GET`** `/api/2.0/brands`

> Returns a paginated list of brands.



#### Responses
**200** 

Body (_Brand Collection_) 
```
{
  "data": [
    {
      "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
      "name": "Peak Performance",
      "deleted_at": "2014-07-01T20:22:58+00:00",
      "version": 1288421
    }
  ]
}
```


[Back to API Reference](#api_reference)

## <a name="customers"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Customers") Customers


### <a name="list_customers"></a>![Endpoint: ](https://apidocs.io/img/method.png "List customers") List customers


**`GET`** `/api/2.0/customers`

> Returns a paginated list of customers.



#### Responses
**200** 

Body (_Customer Collection_) 
```
{
  "data": [
    {
      "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
      "customer_code": "Tony-QKG3",
      "customer_group_id": "b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4",
      "enable_loyalty": true,
      "first_name": "Tony",
      "last_name": "Stark",
      "email": "ironman@avengers.com",
      "note": "",
      "gender": "M",
      "date_of_birth": "1963-03-03",
      "company_name": "Stark Inc.",
      "phone": "",
      "mobile": "",
      "fax": "",
      "twitter": "",
      "website": "",
      "physical_address_1": "",
      "physical_address_2": "",
      "physical_suburb": "",
      "physical_city": "",
      "physical_postcode": "",
      "physical_state": "",
      "physical_country_id": "US",
      "postal_address_1": "",
      "postal_address_2": "",
      "postal_suburb": "",
      "postal_city": "",
      "postal_postcode": "",
      "postal_state": "",
      "postal_country_id": "",
      "custom_field_1": "",
      "custom_field_2": "",
      "custom_field_3": "",
      "custom_field_4": "",
      "name": "Tony Stark",
      "year_to_date": 0,
      "balance": 0,
      "loyalty_balance": 0,
      "created_at": "2014-06-09T21:04:50+00:00",
      "updated_at": "2014-06-09T21:04:50+00:00",
      "deleted_at": "2014-07-01T20:22:58+00:00",
      "version": 1288421
    }
  ]
}
```


### <a name="create_a_new_customer"></a>![Endpoint: ](https://apidocs.io/img/method.png "Create a new customer") Create a new customer


**`POST`** `/api/2.0/customers`

> Creates a new customer.



#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| `customer base` |  ``` Required ```  | TODO: Add a parameter description | 

 Example 
``` 
{
  "customer_code": "Tony-QKG3",
  "customer_group_id": "b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4",
  "enable_loyalty": true,
  "first_name": "Tony",
  "last_name": "Stark",
  "email": "ironman@avengers.com",
  "note": "",
  "gender": "M",
  "date_of_birth": "1963-03-03",
  "company_name": "Stark Inc.",
  "phone": "",
  "mobile": "",
  "fax": "",
  "twitter": "",
  "website": "",
  "physical_address_1": "",
  "physical_address_2": "",
  "physical_suburb": "",
  "physical_city": "",
  "physical_postcode": "",
  "physical_state": "",
  "physical_country_id": "US",
  "postal_address_1": "",
  "postal_address_2": "",
  "postal_suburb": "",
  "postal_city": "",
  "postal_postcode": "",
  "postal_state": "",
  "postal_country_id": "",
  "custom_field_1": "",
  "custom_field_2": "",
  "custom_field_3": "",
  "custom_field_4": ""
}
``` 

#### Responses
**200** 

Body (_Customer Response_) 
```
{
  "data": {
    "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
    "customer_code": "Tony-QKG3",
    "customer_group_id": "b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4",
    "enable_loyalty": true,
    "first_name": "Tony",
    "last_name": "Stark",
    "email": "ironman@avengers.com",
    "note": "",
    "gender": "M",
    "date_of_birth": "1963-03-03",
    "company_name": "Stark Inc.",
    "phone": "",
    "mobile": "",
    "fax": "",
    "twitter": "",
    "website": "",
    "physical_address_1": "",
    "physical_address_2": "",
    "physical_suburb": "",
    "physical_city": "",
    "physical_postcode": "",
    "physical_state": "",
    "physical_country_id": "US",
    "postal_address_1": "",
    "postal_address_2": "",
    "postal_suburb": "",
    "postal_city": "",
    "postal_postcode": "",
    "postal_state": "",
    "postal_country_id": "",
    "custom_field_1": "",
    "custom_field_2": "",
    "custom_field_3": "",
    "custom_field_4": "",
    "name": "Tony Stark",
    "year_to_date": 0,
    "balance": 0,
    "loyalty_balance": 0,
    "created_at": "2014-06-09T21:04:50+00:00",
    "updated_at": "2014-06-09T21:04:50+00:00",
    "deleted_at": "2014-07-01T20:22:58+00:00",
    "version": 1288421
  }
}
```


### <a name="get_a_single_customer"></a>![Endpoint: ](https://apidocs.io/img/method.png "Get a single customer") Get a single customer


**`GET`** `/api/2.0/customers/{customer_id}`

> Returns a single customer with a requested `id`.



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| customer_id | `uuid` |  ``` Required ```  | Valid customer `id`. | `"6c1b4de0-4f24-40ed-a428-c91577fc2e8d"` | 

#### Responses
**200** 

Body (_Customer Response_) 
```
{
  "data": {
    "name": "name",
    "year_to_date": 254.936084579647,
    "balance": 254.936084579647,
    "loyalty_balance": 254.936084579647,
    "customer_code": "customer_code",
    "customer_group_id": "customer_group_id",
    "enable_loyalty": true,
    "first_name": "first_name",
    "last_name": "last_name",
    "email": "email",
    "note": "note",
    "gender": "gender",
    "date_of_birth": "date_of_birth",
    "company_name": "company_name",
    "phone": "phone",
    "mobile": "mobile",
    "fax": "fax",
    "twitter": "twitter",
    "website": "website",
    "physical_address_1": "physical_address_1",
    "physical_address_2": "physical_address_2",
    "physical_suburb": "physical_suburb",
    "physical_city": "physical_city",
    "physical_postcode": "physical_postcode",
    "physical_state": "physical_state",
    "physical_country_id": "physical_country_id",
    "postal_address_1": "postal_address_1",
    "postal_address_2": "postal_address_2",
    "postal_suburb": "postal_suburb",
    "postal_city": "postal_city",
    "postal_postcode": "postal_postcode",
    "postal_state": "postal_state",
    "postal_country_id": "postal_country_id",
    "custom_field_1": "custom_field_1",
    "custom_field_2": "custom_field_2",
    "custom_field_3": "custom_field_3",
    "custom_field_4": "custom_field_4"
  }
}
```


### <a name="update_a_customer"></a>![Endpoint: ](https://apidocs.io/img/method.png "Update a customer") Update a customer


**`PUT`** `/api/2.0/customers/{customer_id}`

> Updates editable fields for the customer with the requested `id`.



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| customer_id | `uuid` |  ``` Required ```  | Valid customer `id`. | `"91e7260f-bb03-4dab-94f0-b8dd62119bed"` | 

#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| `customer base` |  ``` Required ```  | TODO: Add a parameter description | 

 Example 
``` 
{
  "first_name": "first_name",
  "last_name": "last_name",
  "customer_code": "customer_code",
  "customer_group_id": "customer_group_id",
  "enable_loyalty": true,
  "email": "email",
  "note": "note",
  "gender": "gender",
  "date_of_birth": "date_of_birth",
  "company_name": "company_name",
  "phone": "phone",
  "mobile": "mobile",
  "fax": "fax",
  "twitter": "twitter",
  "website": "website",
  "physical_address_1": "physical_address_1",
  "physical_address_2": "physical_address_2",
  "physical_suburb": "physical_suburb",
  "physical_city": "physical_city",
  "physical_postcode": "physical_postcode",
  "physical_state": "physical_state",
  "physical_country_id": "physical_country_id",
  "postal_address_1": "postal_address_1",
  "postal_address_2": "postal_address_2",
  "postal_suburb": "postal_suburb",
  "postal_city": "postal_city",
  "postal_postcode": "postal_postcode",
  "postal_state": "postal_state",
  "postal_country_id": "postal_country_id",
  "custom_field_1": "custom_field_1",
  "custom_field_2": "custom_field_2",
  "custom_field_3": "custom_field_3",
  "custom_field_4": "custom_field_4"
}
``` 

#### Responses
**200** 

Body (_Customer Response_) 
```
{
  "data": {
    "name": "name",
    "year_to_date": 254.936084579647,
    "balance": 254.936084579647,
    "loyalty_balance": 254.936084579647,
    "customer_code": "customer_code",
    "customer_group_id": "customer_group_id",
    "enable_loyalty": true,
    "first_name": "first_name",
    "last_name": "last_name",
    "email": "email",
    "note": "note",
    "gender": "gender",
    "date_of_birth": "date_of_birth",
    "company_name": "company_name",
    "phone": "phone",
    "mobile": "mobile",
    "fax": "fax",
    "twitter": "twitter",
    "website": "website",
    "physical_address_1": "physical_address_1",
    "physical_address_2": "physical_address_2",
    "physical_suburb": "physical_suburb",
    "physical_city": "physical_city",
    "physical_postcode": "physical_postcode",
    "physical_state": "physical_state",
    "physical_country_id": "physical_country_id",
    "postal_address_1": "postal_address_1",
    "postal_address_2": "postal_address_2",
    "postal_suburb": "postal_suburb",
    "postal_city": "postal_city",
    "postal_postcode": "postal_postcode",
    "postal_state": "postal_state",
    "postal_country_id": "postal_country_id",
    "custom_field_1": "custom_field_1",
    "custom_field_2": "custom_field_2",
    "custom_field_3": "custom_field_3",
    "custom_field_4": "custom_field_4"
  }
}
```


### <a name="delete_a_customer"></a>![Endpoint: ](https://apidocs.io/img/method.png "Delete a customer") Delete a customer


**`DELETE`** `/api/2.0/customers/{customer_id}`

> Deletes the customer with the requested `id`.



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| customer_id | `uuid` |  ``` Required ```  | Valid customer `id`. | `"17fa0dcd-bec1-4cb8-95d2-c8473853bf3f"` | 

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="customer_groups"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Customer Groups") Customer Groups


### <a name="list_customer_groups"></a>![Endpoint: ](https://apidocs.io/img/method.png "List customer groups") List customer groups


**`GET`** `/api/2.0/customer_groups`

> Returns a paginated list of customer groups.



#### Responses
**200** 

Body (_Customer Group Collection_) 
```
{
  "data": [
    {
      "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
      "name": "Peak Performance",
      "group_id": "1111111111",
      "created_at": "2014-06-09T21:04:50+00:00",
      "updated_at": "2014-06-09T21:04:50+00:00",
      "deleted_at": "2014-07-01T20:22:58+00:00",
      "version": 1288421
    }
  ]
}
```


[Back to API Reference](#api_reference)

## <a name="consignments"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Consignments") Consignments


### <a name="list_consignments"></a>![Endpoint: ](https://apidocs.io/img/method.png "List consignments") List consignments


**`GET`** `/api/2.0/consignments`

> Returns a paginated list of consignments.



#### Responses
**200** 

Body (_Consignment Collection_) 
```
{
  "data": [
    {
      "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
      "outlet_id": "b1e04bd8-f019-11e3-a0f5-b8ca3a64f8f4",
      "name": "Order",
      "consignment_date": "2016",
      "due_at": "2016",
      "received_at": "2016",
      "type": "SUPPLIER",
      "status": "RECEIVED",
      "supplier_id": "b1e04bd8-f019-11e3-a0f5-b8ca3a64f8f4",
      "source_outlet_id": "b1e04bd8-f019-11e3-a0f5-b8ca3a64f8f4",
      "supplier_invoice": "VE1234",
      "reference": "\"test order no\"",
      "total_count_gain": 0,
      "total_cost_gain": 0,
      "total_count_loss": 0,
      "total_cost_loss": 0,
      "created_at": "2014-06-09T21:04:50+00:00",
      "updated_at": "2014-06-09T21:04:50+00:00",
      "deleted_at": "2014-07-01T20:22:58+00:00",
      "version": 1288421
    }
  ]
}
```


### <a name="get_a_single_consignment"></a>![Endpoint: ](https://apidocs.io/img/method.png "Get a single consignment") Get a single consignment


**`GET`** `/api/2.0/consignments/{consignment_id}`

> Returns a single consignment with the requested `id`.



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| consignment_id | `uuid` |  ``` Required ```  | Valid consignment `id`. | `"6a34158c-0ec3-47d8-80aa-f15e2708f4cd"` | 

#### Responses
**200** 

Body (_Consignment Response_) 
```
{
  "data": {
    "total_count_gain": 254.936084579647,
    "total_cost_gain": 254.936084579647,
    "total_count_loss": 254.936084579647,
    "total_cost_loss": 254.936084579647,
    "outlet_id": "outlet_id",
    "name": "name",
    "consignment_date": "consignment_date",
    "due_at": "due_at",
    "received_at": "received_at",
    "type": "type",
    "status": "status",
    "supplier_id": "supplier_id",
    "source_outlet_id": "source_outlet_id",
    "supplier_invoice": "supplier_invoice",
    "reference": "reference"
  }
}
```


[Back to API Reference](#api_reference)

## <a name="inventory"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Inventory") Inventory


### <a name="list_inventory_records"></a>![Endpoint: ](https://apidocs.io/img/method.png "List inventory records") List inventory records


**`GET`** `/api/2.0/inventory`

> Returns a paginated list of Inventory records.



#### Responses
**200** 

Body (_Inventory Collection_) 
```
{
  "data": [
    {
      "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
      "product_id": "b8ca3a65-0183-11e4-fbb5-6ba391393b6e",
      "outlet_id": "b1e04bd8-f019-11e3-a0f5-b8ca3a64f8f4",
      "inventory_level": 39,
      "reorder_point": 10,
      "reorder_amount": 50,
      "version": 1288421
    }
  ]
}
```


[Back to API Reference](#api_reference)

## <a name="outlets"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Outlets") Outlets


### <a name="list_outlets"></a>![Endpoint: ](https://apidocs.io/img/method.png "List outlets") List outlets


**`GET`** `/api/2.0/outlets`

> Returns a collection of outlets.



#### Responses
**200** 

Body (_Outlet Collection_) 
```
{
  "data": [
    {
      "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
      "name": "Main Outlet",
      "time_zone": "Pacific/Auckland",
      "default_tax_id": "b1d192bc-f019-11e3-a0f5-b8ca3a64f8f4",
      "currency": "NZD",
      "currency_symbol": "$",
      "display_prices": "inclusive",
      "deleted_at": "2014-07-01T20:22:58+00:00",
      "version": 1288421
    }
  ]
}
```


### <a name="get_a_single_outlet"></a>![Endpoint: ](https://apidocs.io/img/method.png "Get a single outlet") Get a single outlet


**`GET`** `/api/2.0/outlets/{outlet_id}`

> Returns a single outlet with the requested `id`.



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| outlet_id | `uuid` |  ``` Required ```  | Valid Outlet `id`. | `"30534dd5-f465-4e74-b124-75137dca2d02"` | 

#### Responses
**200** 

Body (_Outlet Collection_) 
```
{
  "data": [
    {
      "name": "name",
      "time_zone": "time_zone",
      "default_tax_id": "default_tax_id",
      "currency": "currency",
      "currency_symbol": "currency_symbol",
      "display_prices": "display_prices"
    }
  ]
}
```


[Back to API Reference](#api_reference)

## <a name="price_books"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Price Books") Price Books


### <a name="list_price_books"></a>![Endpoint: ](https://apidocs.io/img/method.png "List price books") List price books


**`GET`** `/api/2.0/price_books`

> Returns a paginated list of price books



#### Responses
**200** 

Body (_Price Book Collection_) 
```
{
  "data": [
    {
      "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
      "name": "Test",
      "valid_from": "2018-01-01",
      "valid_to": "2019-01-01",
      "restrict_to_platform_key": "1",
      "customer_group_id": "b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4",
      "outlet_id": "",
      "type": "GENERAL",
      "restrict_to_platform_label": "In Store",
      "customer_group": {
        "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
        "name": "Peak Performance",
        "group_id": "1111111111",
        "created_at": "2014-06-09T21:04:50+00:00",
        "updated_at": "2014-06-09T21:04:50+00:00",
        "deleted_at": "2014-07-01T20:22:58+00:00",
        "version": 1288421
      },
      "version": 1288421,
      "deleted_at": "2014-07-01T20:22:58+00:00"
    }
  ]
}
```


### <a name="create_a_price_book"></a>![Endpoint: ](https://apidocs.io/img/method.png "Create a price book") Create a price book


**`POST`** `/api/2.0/price_books`

> Creates a new price book.



#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| `price book base` |  ``` Required ```  | TODO: Add a parameter description | 

 Example 
``` 
{
  "name": "Test",
  "valid_from": "2018-01-01",
  "valid_to": "2019-01-01",
  "restrict_to_platform_key": "1",
  "customer_group_id": "b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4",
  "outlet_id": ""
}
``` 

#### Responses
**200** 

Body (_Price Book Response_) 
```
{
  "data": {
    "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
    "name": "Test",
    "valid_from": "2018-01-01",
    "valid_to": "2019-01-01",
    "restrict_to_platform_key": "1",
    "customer_group_id": "b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4",
    "outlet_id": "",
    "type": "GENERAL",
    "restrict_to_platform_label": "In Store",
    "customer_group": {
      "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
      "name": "Peak Performance",
      "group_id": "1111111111",
      "created_at": "2014-06-09T21:04:50+00:00",
      "updated_at": "2014-06-09T21:04:50+00:00",
      "deleted_at": "2014-07-01T20:22:58+00:00",
      "version": 1288421
    },
    "version": 1288421,
    "deleted_at": "2014-07-01T20:22:58+00:00"
  }
}
```


### <a name="get_a_single_price_book"></a>![Endpoint: ](https://apidocs.io/img/method.png "Get a single price book") Get a single price book


**`GET`** `/api/2.0/price_books/{price_book_id}`

> Returns a single price book with a requested `id`



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| price_book_id | `uuid` |  ``` Required ```  | Valid price book `id`. | `"38f3f237-2439-48a3-ac34-c6c160228020"` | 

#### Responses
**200** 

Body (_Price Book Response_) 
```
{
  "data": {
    "type": "type",
    "restrict_to_platform_label": "restrict_to_platform_label",
    "customer_group": {
      "name": "name",
      "group_id": "group_id"
    },
    "name": "name",
    "valid_from": "valid_from",
    "valid_to": "valid_to",
    "restrict_to_platform_key": "restrict_to_platform_key",
    "customer_group_id": "customer_group_id",
    "outlet_id": "outlet_id"
  }
}
```


[Back to API Reference](#api_reference)

## <a name="price_book_products"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Price Book Products") Price Book Products


### <a name="list_price_book_products"></a>![Endpoint: ](https://apidocs.io/img/method.png "List price book products") List price book products


**`GET`** `/api/2.0/price_book_products`

> Returns a paginated list of price book products.



#### Responses
**200** 

Body (_Price Book Product Collection_) 
```
{
  "data": [
    {
      "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
      "name": "Test",
      "valid_from": "2018-01-01",
      "valid_to": "2019-01-01",
      "restrict_to_platform_key": "1",
      "customer_group_id": "b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4",
      "outlet_id": "",
      "version": 1288421,
      "created_at": "2014-06-09T21:04:50+00:00",
      "updated_at": "2014-06-09T21:04:50+00:00",
      "deleted_at": "2014-07-01T20:22:58+00:00"
    }
  ]
}
```


[Back to API Reference](#api_reference)

## <a name="products"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Products") Products


### <a name="list_products"></a>![Endpoint: ](https://apidocs.io/img/method.png "List products") List products


**`GET`** `/api/2.0/products`

> Returns a paginated list of products.



#### Responses
**200** 

Body (_Product Collection_) 
```
{
  "data": [
    {
      "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
      "source_id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
      "source_variant_id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
      "variant_parent_id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
      "name": "Bravo",
      "handle": "bravo",
      "sku": "sku123456",
      "source": "USER",
      "active": true,
      "has_inventory": true,
      "is_composite": false,
      "has_variants": false,
      "description": "<p>Product Description</p>",
      "supplier_code": "PEAK",
      "supply_price": 100,
      "type": {
        "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
        "name": "General",
        "deleted_at": "2014-07-01T20:22:58+00:00",
        "version": 1288421
      },
      "supplier": {
        "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
        "name": "Peak Inc.",
        "deleted_at": "2014-07-01T20:22:58+00:00",
        "version": 1288421
      },
      "brand": {
        "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
        "name": "Peak Performance",
        "deleted_at": "2014-07-01T20:22:58+00:00",
        "version": 1288421
      },
      "variant_options": [
        {
          "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
          "name": "Color",
          "value": "Black"
        }
      ],
      "categories": [
        {
          "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
          "name": "tag_test",
          "deleted_at": "2014-07-01T20:22:58+00:00",
          "version": 1288421
        },
        {
          "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
          "name": "another_tag",
          "deleted_at": "2014-07-01T20:22:58+00:00",
          "version": 1288421
        }
      ],
      "variant_name": "Bravo / Black",
      "image_url": "https://s3.amazonaws.com/vend-images/product/standard/f/0/f0ebadbc30947444d438678a4a7bd6d996f392fc.jpg",
      "image_thumbnail_url": "https://s3.amazonaws.com/vend-images/product/thumb/f/0/f0ebadbc30947444d438678a4a7bd6d996f392fc.jpg",
      "images": [
        {
          "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
          "url": "https://s3.amazonaws.com/vend-images/product/standard/f/0/f0ebadbc30947444d438678a4a7bd6d996f392fc.jpg",
          "version": 1288421
        }
      ],
      "created_at": "2014-06-09T21:04:50+00:00",
      "updated_at": "2014-06-09T21:04:50+00:00",
      "deleted_at": "2014-07-01T20:22:58+00:00",
      "version": 1288421
    }
  ]
}
```


### <a name="get_a_single_product"></a>![Endpoint: ](https://apidocs.io/img/method.png "Get a single product") Get a single product


**`GET`** `/api/2.0/products/{product_id}`

> Returns a single product object with a given `id`.



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| product_id | `uuid` |  ``` Required ```  | Valid product `id`. | `"de6c7854-f708-4fa5-9233-6f939eae6763"` | 

#### Responses
**200** 

Body (_Product Response_) 
```
{
  "data": {
    "variant_name": "variant_name",
    "image_url": "image_url",
    "image_thumbnail_url": "image_thumbnail_url",
    "images": [
      {
        "url": "url"
      }
    ],
    "source_id": "source_id",
    "source_variant_id": "source_variant_id",
    "variant_parent_id": "variant_parent_id",
    "name": "name",
    "handle": "handle",
    "sku": "sku",
    "source": "source",
    "active": true,
    "has_inventory": true,
    "is_composite": true,
    "has_variants": true,
    "description": "description",
    "supplier_code": "supplier_code",
    "supply_price": 254.936084579647,
    "type": {
      "name": "name"
    },
    "supplier": {
      "name": "name"
    },
    "brand": {
      "name": "name"
    },
    "variant_options": [
      {
        "name": "name",
        "value": "value"
      }
    ],
    "categories": [
      {
        "name": "name"
      }
    ]
  }
}
```


### <a name="get_inventory_data_for_a_single_product"></a>![Endpoint: ](https://apidocs.io/img/method.png "Get inventory data for a single product") Get inventory data for a single product


**`GET`** `/api/2.0/products/{product_id}/inventory`

> Returns inventory data for a single product in all the outlets.



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| product_id | `uuid` |  ``` Required ```  | Valid product `id`. | `"52244e1c-8b97-4fde-9d90-198fd7fc6154"` | 

#### Responses
**200** 

Body (_Inventory Collection_) 
```
{
  "data": [
    {
      "product_id": "product_id",
      "outlet_id": "outlet_id",
      "inventory_level": 254.936084579647,
      "reorder_point": 254.936084579647,
      "reorder_amount": 254.936084579647
    }
  ]
}
```


### <a name="upload_an_image"></a>![Endpoint: ](https://apidocs.io/img/method.png "Upload an image") Upload an image


**`POST`** `/api/2.0/products/{product_id}/actions/image_upload`

> Upload a binary file with an image to be used for a product.



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| product_id | `string` |  ``` Optional ```  | TODO: Add a parameter description | `"product_id"` | 

#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| `upload an image request` |  ``` Required ```  | TODO: Add a parameter description | 

 Example 
``` 
{
  "image": "image"
}
``` 

#### Responses
**200** 

Body (_Image Response_) 
```
{
  "data": {
    "Inlucde Image Base": "Inlucde Image Base"
  }
}
```


[Back to API Reference](#api_reference)

## <a name="product_images"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Product Images") Product Images


### <a name="get_a_single_product_image_data"></a>![Endpoint: ](https://apidocs.io/img/method.png "Get a single product_image data") Get a single product_image data


**`GET`** `/api/2.0/product_images/{product_image_id}`

> Returns the metadata for a single product image with a given `id`.
> This method is useful for checking the status of an image after it was uploaded.



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| product_image_id | `uuid` |  ``` Required ```  | Valid product `id`. | `"ca8a9805-7642-4fc8-ac52-5784b3887a36"` | 

#### Responses
**200** 

Body (_Image Response_) 
```
{
  "data": {
    "Inlucde Image Base": "Inlucde Image Base"
  }
}
```


### <a name="set_image_position"></a>![Endpoint: ](https://apidocs.io/img/method.png "Set image position") Set image position


**`PUT`** `/api/2.0/product_images/{product_image_id}`

> Allows for changing the image position in the list



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| product_image_id | `string` |  ``` Optional ```  | TODO: Add a parameter description | `"product_image_id"` | 

#### Request Headers
>Accept=application/json;
>Content-Type=application/json;

#### Request Body
Raw 

|  Type | Tags | Description |
| ------| ---- |-------------| 
| `image position` |  ``` Required ```  | TODO: Add a parameter description | 

 Example 
``` 
{
  "position": 1
}
``` 

#### Responses
**200** 

Body (_Image Response_) 
```
{
  "data": {
    "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
    "Inlucde Image Base": "",
    "version": 1288421
  }
}
```


### <a name="delete_a_product_image"></a>![Endpoint: ](https://apidocs.io/img/method.png "Delete a product_image") Delete a product_image


**`DELETE`** `/api/2.0/product_images/{product_image_id}`

> Deletes the product_image with the requested `id`.



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| product_image_id | `string` |  ``` Optional ```  | TODO: Add a parameter description | `"product_image_id"` | 

#### Responses
**200**


[Back to API Reference](#api_reference)

## <a name="product_types"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Product Types") Product Types


### <a name="list_product_types"></a>![Endpoint: ](https://apidocs.io/img/method.png "List product types") List product types


**`GET`** `/api/2.0/product_types`

> Returns a paginated list of product types.



#### Responses
**200** 

Body (_Product Type Collection_) 
```
{
  "data": [
    {
      "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
      "name": "sportswear",
      "deleted_at": "2014-07-01T20:22:58+00:00",
      "version": 1288421
    }
  ]
}
```


[Back to API Reference](#api_reference)

## <a name="registers"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Registers") Registers


### <a name="list_registers"></a>![Endpoint: ](https://apidocs.io/img/method.png "List registers") List registers


**`GET`** `/api/2.0/registers`

> Returns a paginated list of registers.



#### Responses
**200** 

Body (_Register Collection_) 
```
{
  "data": [
    {
      "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
      "name": "Main Register",
      "outlet_id": "b8ca3a65-0183-11e4-fbb5-2816d2677218",
      "ask_for_note_on_save": 1,
      "print_note_on_receipt": false,
      "ask_for_user_on_sale": false,
      "show_discounts_on_receipts": true,
      "print_receipt": true,
      "email_receipt": false,
      "invoice_prefix": "PRE",
      "invoice_suffix": "SUF",
      "invoice_sequence": 1234,
      "button_layout_id": "b8ca3a65-0183-11e4-fbb5-2816e25ffc51",
      "is_open": true,
      "register_open_time": "2015-03-16T22:21:50+00:00",
      "register_close_time": "null",
      "deleted_at": "2014-07-01T20:22:58+00:00",
      "version": 1288421
    }
  ]
}
```


### <a name="get_a_single_register"></a>![Endpoint: ](https://apidocs.io/img/method.png "Get a single register") Get a single register


**`GET`** `/api/2.0/registers/{register_id}`

> Returns a single register with the requested `id`.



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| register_id | `uuid` |  ``` Required ```  | Valid register `id`. | `"8bcf626c-ae99-472e-96f9-a9d90d22b8a1"` | 

#### Responses
**200** 

Body (_Register Collection_) 
```
{
  "data": [
    {
      "button_layout_id": "button_layout_id",
      "is_open": true,
      "register_open_time": "register_open_time",
      "register_close_time": "register_close_time",
      "name": "name",
      "outlet_id": "outlet_id",
      "ask_for_note_on_save": 254.936084579647,
      "print_note_on_receipt": true,
      "ask_for_user_on_sale": true,
      "show_discounts_on_receipts": true,
      "print_receipt": true,
      "email_receipt": true,
      "invoice_prefix": "invoice_prefix",
      "invoice_suffix": "invoice_suffix",
      "invoice_sequence": 254.936084579647
    }
  ]
}
```


[Back to API Reference](#api_reference)

## <a name="tags"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Tags") Tags


### <a name="list_tags"></a>![Endpoint: ](https://apidocs.io/img/method.png "List tags") List tags


**`GET`** `/api/2.0/tags`

> Returns a collection of tags.



#### Responses
**200** 

Body (_Tag Collection_) 
```
{
  "data": [
    {
      "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
      "name": "Peak Performance",
      "deleted_at": "2014-07-01T20:22:58+00:00",
      "version": 1288421
    }
  ]
}
```


[Back to API Reference](#api_reference)

## <a name="sales"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Sales") Sales


### <a name="list_sales"></a>![Endpoint: ](https://apidocs.io/img/method.png "List Sales") List Sales


**`GET`** `/api/2.0/sales`

> Returns a paginated list of Sales.



#### Responses
**200** 

Body (_Sale Collection_) 
```
{
  "data": [
    {
      "register_id": "b1e198a9-f019-11e3-a0f5-b8ca3a64f8f4",
      "user_id": "b1ed6158-f019-11e3-a0f5-b8ca3a64f8f4",
      "customer_id": "b1cabb53-f019-11e3-a0f5-b8ca3a64f8f4",
      "invoice_number": "SP-1036-R1",
      "invoice_sequence": 1213,
      "status": "CLOSED",
      "note": "",
      "short_code": "xamfvy",
      "sale_date": "2014-09-18T01:37:56+00:00",
      "line_items": [
        {
          "product_id": "188a87aa-06fe-11e4-a0f5-b8ca3a64f8f4",
          "quantity": 1,
          "price": 123.45678,
          "discount": 0,
          "loyalty_value": 0,
          "price_set": false,
          "sequence": 0,
          "note": "",
          "status": "CONFIRMED",
          "tax_components": [
            {
              "rate_id": "b1dfed8b-f019-11e3-a0f5-b8ca3a64f8f4",
              "total_tax": 0
            }
          ],
          "tax_id": "b1d192bc-f019-11e3-a0f5-b8ca3a64f8f4",
          "discount_total": 0,
          "is_return": false,
          "cost": 100,
          "cost_total": 100,
          "price_total": 0,
          "tax": 0,
          "tax_total": 0
        }
      ],
      "payments": [
        {
          "register_id": "b1e198a9-f019-11e3-a0f5-b8ca3a64f8f4",
          "retailer_payment_type_id": "1e1d70e-f019-11e3-a0f5-b8ca3a64f8f4",
          "payment_type_id": "1",
          "payment_date": "2014-09-18T01:37:54+00:00",
          "amount": 230,
          "name": "Cash"
        }
      ],
      "outlet_id": "b1e198a9-f019-11e3-a0f5-b8ca3a64f8f4",
      "return_for": "b1cabb53-f019-11e3-a0f5-b8ca3a64f8f4",
      "total_price": 200,
      "total_tax": 30,
      "deleted_at": "2014-07-01T20:22:58+00:00",
      "version": 1288421,
      "taxes": [
        {
          "name": "GST",
          "rate": 0.15,
          "amount": 30
        }
      ]
    }
  ]
}
```


[Back to API Reference](#api_reference)

## <a name="suppliers"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "Suppliers") Suppliers


### <a name="list_suppliers"></a>![Endpoint: ](https://apidocs.io/img/method.png "List suppliers") List suppliers


**`GET`** `/api/2.0/suppliers`

> Returns a paginated list of suppliers.



#### Responses
**200** 

Body (_Supplier Collection_) 
```
{
  "data": [
    {
      "id": "dc85058a-a683-11e4-ef46-e8b98f1a7ae4",
      "name": "ICCompanies",
      "deleted_at": "2014-07-01T20:22:58+00:00",
      "version": 1288421
    }
  ]
}
```


[Back to API Reference](#api_reference)

