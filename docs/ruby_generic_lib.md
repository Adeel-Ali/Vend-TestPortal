# Getting started

TODO: Add a description

## How to Build

This client library is a Ruby gem which can be compiled and used in your Ruby and Ruby on Rails project. This library requires a few gems from the RubyGems repository.

1. Open the command line interface or the terminal and navigate to the folder containing the source code.
2. Run ``` gem build vend_restapi_20.gemspec ``` to build the gem.
3. Once built, the gem can be installed on the current work environment using ``` gem install vend_restapi_20-1.0.0.gem ```

![Building Gem](https://apidocs.io/illustration/ruby?step=buildSDK&workspaceFolder=Vend%20REST%20API%202.0-Ruby&workspaceName=Vend%20REST%20API%202.0-Ruby&projectName=vend_restapi_20&gemName=vend_restapi_20&gemVer=1.0.0)

## How to Use

The following section explains how to use the VendRestapi20 Ruby Gem in a new Rails project using RubyMine&trade;. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

### 1. Starting a new project

Close any existing projects in RubyMine&trade; by selecting ``` File -> Close Project ```. Next, click on ``` Create New Project ``` to create a new project from scratch.

![Create a new project in RubyMine](https://apidocs.io/illustration/ruby?step=createNewProject0&workspaceFolder=Vend%20REST%20API%202.0-Ruby&workspaceName=VendRestapi20&projectName=vend_restapi_20&gemName=vend_restapi_20&gemVer=1.0.0)

Next, provide ``` TestApp ``` as the project name, choose ``` Rails Application ``` as the project type, and click ``` OK ```.

![Create a new Rails Application in RubyMine - step 1](https://apidocs.io/illustration/ruby?step=createNewProject1&workspaceFolder=Vend%20REST%20API%202.0-Ruby&workspaceName=VendRestapi20&projectName=vend_restapi_20&gemName=vend_restapi_20&gemVer=1.0.0)

In the next dialog make sure that correct *Ruby SDK* is being used (minimum 2.0.0) and click ``` OK ```.

![Create a new Rails Application in RubyMine - step 2](https://apidocs.io/illustration/ruby?step=createNewProject2&workspaceFolder=Vend%20REST%20API%202.0-Ruby&workspaceName=VendRestapi20&projectName=vend_restapi_20&gemName=vend_restapi_20&gemVer=1.0.0)

This will create a new Rails Application project with an existing set of files and folder.

### 2. Add reference of the gem

In order to use the VendRestapi20 gem in the new project we must add a gem reference. Locate the ```Gemfile``` in the *Project Explorer* window under the ``` TestApp ``` project node. The file contains references to all gems being used in the project. Here, add the reference to the library gem by adding the following line: ``` gem 'vend_restapi_20', '~> 1.0.0' ```

![Add references of the Gemfile](https://apidocs.io/illustration/ruby?step=addReference&workspaceFolder=Vend%20REST%20API%202.0-Ruby&workspaceName=VendRestapi20&projectName=vend_restapi_20&gemName=vend_restapi_20&gemVer=1.0.0)

### 3. Adding a new Rails Controller

Once the ``` TestApp ``` project is created, a folder named ``` controllers ``` will be visible in the *Project Explorer* under the following path: ``` TestApp > app > controllers ```. Right click on this folder and select ``` New -> Run Rails Generator... ```.

![Run Rails Generator on Controllers Folder](https://apidocs.io/illustration/ruby?step=addCode0&workspaceFolder=Vend%20REST%20API%202.0-Ruby&workspaceName=VendRestapi20&projectName=vend_restapi_20&gemName=vend_restapi_20&gemVer=1.0.0)

Selecting the said option will popup a small window where the generator names are displayed. Here, select the ``` controller ``` template.

![Create a new Controller](https://apidocs.io/illustration/ruby?step=addCode1&workspaceFolder=Vend%20REST%20API%202.0-Ruby&workspaceName=VendRestapi20&projectName=vend_restapi_20&gemName=vend_restapi_20&gemVer=1.0.0)

Next, a popup window will ask you for a Controller name and included Actions. For controller name provide ``` Hello ``` and include an action named ``` Index ``` and click ``` OK ```.

![Add a new Controller](https://apidocs.io/illustration/ruby?step=addCode2&workspaceFolder=Vend%20REST%20API%202.0-Ruby&workspaceName=VendRestapi20&projectName=vend_restapi_20&gemName=vend_restapi_20&gemVer=1.0.0)

A new controller class anmed ``` HelloController ``` will be created in a file named ``` hello_controller.rb ``` containing a method named ``` Index ```. In this method, add code for initialization and a sample for its usage.

![Initialize the library](https://apidocs.io/illustration/ruby?step=addCode3&workspaceFolder=Vend%20REST%20API%202.0-Ruby&workspaceName=VendRestapi20&projectName=vend_restapi_20&gemName=vend_restapi_20&gemVer=1.0.0)

## How to Test

You can test the generated SDK and the server with automatically generated test
cases as follows:

  1. From terminal/cmd navigate to the root directory of the SDK.
  2. Invoke: `bundle exec rake`

## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| o_auth_access_token | OAuth 2.0 Access Token |



API client can be initialized as following.

```ruby
# Configuration parameters and credentials
o_auth_access_token = 'o_auth_access_token' # OAuth 2.0 Access Token

client = VendRestapi20::VendRestapi20Client.new(
  o_auth_access_token: o_auth_access_token
)
```

The added initlization code can be debugged by putting a breakpoint in the ``` Index ``` method and running the project in debug mode by selecting ``` Run -> Debug 'Development: TestApp' ```.

![Debug the TestApp](https://apidocs.io/illustration/ruby?step=addCode4&workspaceFolder=Vend%20REST%20API%202.0-Ruby&workspaceName=VendRestapi20&projectName=vend_restapi_20&gemName=vend_restapi_20&gemVer=1.0.0&initLine=client%2520%253D%2520VendRestapi20Client.new%2528%2527o_auth_access_token%2527%2529)



# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [BrandsController](#brands_controller)
* [CustomersController](#customers_controller)
* [CustomerGroupsController](#customer_groups_controller)
* [ConsignmentsController](#consignments_controller)
* [InventoryController](#inventory_controller)
* [OutletsController](#outlets_controller)
* [PriceBooksController](#price_books_controller)
* [PriceBookProductsController](#price_book_products_controller)
* [ProductsController](#products_controller)
* [ProductImagesController](#product_images_controller)
* [ProductTypesController](#product_types_controller)
* [RegistersController](#registers_controller)
* [TagsController](#tags_controller)
* [SalesController](#sales_controller)
* [SuppliersController](#suppliers_controller)

## <a name="brands_controller"></a>![Class: ](https://apidocs.io/img/class.png ".BrandsController") BrandsController

### Get singleton instance

The singleton instance of the ``` BrandsController ``` class can be accessed from the API Client.

```ruby
brands = client.brands
```

### <a name="list_brands"></a>![Method: ](https://apidocs.io/img/method.png ".BrandsController.list_brands") list_brands

> Returns a paginated list of brands.


```ruby
def list_brands; end
```

#### Example Usage

```ruby

result = brands.list_brands()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="customers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CustomersController") CustomersController

### Get singleton instance

The singleton instance of the ``` CustomersController ``` class can be accessed from the API Client.

```ruby
customers = client.customers
```

### <a name="list_customers"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.list_customers") list_customers

> Returns a paginated list of customers.


```ruby
def list_customers; end
```

#### Example Usage

```ruby

result = customers.list_customers()

```


### <a name="create_a_new_customer"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.create_a_new_customer") create_a_new_customer

> Creates a new customer.


```ruby
def create_a_new_customer(body); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body_value = "{  \"customer_code\": \"Tony-QKG3\",  \"customer_group_id\": \"b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4\",  \"enable_loyalty\": true,  \"first_name\": \"Tony\",  \"last_name\": \"Stark\",  \"email\": \"ironman@avengers.com\",  \"note\": \"\",  \"gender\": \"M\",  \"date_of_birth\": \"1963-03-03\",  \"company_name\": \"Stark Inc.\",  \"phone\": \"\",  \"mobile\": \"\",  \"fax\": \"\",  \"twitter\": \"\",  \"website\": \"\",  \"physical_address_1\": \"\",  \"physical_address_2\": \"\",  \"physical_suburb\": \"\",  \"physical_city\": \"\",  \"physical_postcode\": \"\",  \"physical_state\": \"\",  \"physical_country_id\": \"US\",  \"postal_address_1\": \"\",  \"postal_address_2\": \"\",  \"postal_suburb\": \"\",  \"postal_city\": \"\",  \"postal_postcode\": \"\",  \"postal_state\": \"\",  \"postal_country_id\": \"\",  \"custom_field_1\": \"\",  \"custom_field_2\": \"\",  \"custom_field_3\": \"\",  \"custom_field_4\": \"\"}";
body = JSON.parse(body_value);

result = customers.create_a_new_customer(body)

```


### <a name="get_a_single_customer"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.get_a_single_customer") get_a_single_customer

> Returns a single customer with a requested `id`.


```ruby
def get_a_single_customer(customer_id); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customer_id |  ``` Required ```  | Valid customer `id`. |


#### Example Usage

```ruby
customer_id = UUID.new

result = customers.get_a_single_customer(customer_id)

```


### <a name="update_a_customer"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.update_a_customer") update_a_customer

> Updates editable fields for the customer with the requested `id`.


```ruby
def update_a_customer(customer_id,
                          body); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customer_id |  ``` Required ```  | Valid customer `id`. |
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
customer_id = UUID.new
body = CustomerBase.new

result = customers.update_a_customer(customer_id, body)

```


### <a name="delete_a_customer"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.delete_a_customer") delete_a_customer

> Deletes the customer with the requested `id`.


```ruby
def delete_a_customer(customer_id); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customer_id |  ``` Required ```  | Valid customer `id`. |


#### Example Usage

```ruby
customer_id = UUID.new

customers.delete_a_customer(customer_id)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="customer_groups_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CustomerGroupsController") CustomerGroupsController

### Get singleton instance

The singleton instance of the ``` CustomerGroupsController ``` class can be accessed from the API Client.

```ruby
customerGroups = client.customer_groups
```

### <a name="list_customer_groups"></a>![Method: ](https://apidocs.io/img/method.png ".CustomerGroupsController.list_customer_groups") list_customer_groups

> Returns a paginated list of customer groups.


```ruby
def list_customer_groups; end
```

#### Example Usage

```ruby

result = customerGroups.list_customer_groups()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="consignments_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ConsignmentsController") ConsignmentsController

### Get singleton instance

The singleton instance of the ``` ConsignmentsController ``` class can be accessed from the API Client.

```ruby
consignments = client.consignments
```

### <a name="list_consignments"></a>![Method: ](https://apidocs.io/img/method.png ".ConsignmentsController.list_consignments") list_consignments

> Returns a paginated list of consignments.


```ruby
def list_consignments; end
```

#### Example Usage

```ruby

result = consignments.list_consignments()

```


### <a name="get_a_single_consignment"></a>![Method: ](https://apidocs.io/img/method.png ".ConsignmentsController.get_a_single_consignment") get_a_single_consignment

> Returns a single consignment with the requested `id`.


```ruby
def get_a_single_consignment(consignment_id); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| consignment_id |  ``` Required ```  | Valid consignment `id`. |


#### Example Usage

```ruby
consignment_id = UUID.new

result = consignments.get_a_single_consignment(consignment_id)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="inventory_controller"></a>![Class: ](https://apidocs.io/img/class.png ".InventoryController") InventoryController

### Get singleton instance

The singleton instance of the ``` InventoryController ``` class can be accessed from the API Client.

```ruby
inventory = client.inventory
```

### <a name="list_inventory_records"></a>![Method: ](https://apidocs.io/img/method.png ".InventoryController.list_inventory_records") list_inventory_records

> Returns a paginated list of Inventory records.


```ruby
def list_inventory_records; end
```

#### Example Usage

```ruby

result = inventory.list_inventory_records()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="outlets_controller"></a>![Class: ](https://apidocs.io/img/class.png ".OutletsController") OutletsController

### Get singleton instance

The singleton instance of the ``` OutletsController ``` class can be accessed from the API Client.

```ruby
outlets = client.outlets
```

### <a name="list_outlets"></a>![Method: ](https://apidocs.io/img/method.png ".OutletsController.list_outlets") list_outlets

> Returns a collection of outlets.


```ruby
def list_outlets; end
```

#### Example Usage

```ruby

result = outlets.list_outlets()

```


### <a name="get_a_single_outlet"></a>![Method: ](https://apidocs.io/img/method.png ".OutletsController.get_a_single_outlet") get_a_single_outlet

> Returns a single outlet with the requested `id`.


```ruby
def get_a_single_outlet(outlet_id); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| outlet_id |  ``` Required ```  | Valid Outlet `id`. |


#### Example Usage

```ruby
outlet_id = UUID.new

result = outlets.get_a_single_outlet(outlet_id)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="price_books_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PriceBooksController") PriceBooksController

### Get singleton instance

The singleton instance of the ``` PriceBooksController ``` class can be accessed from the API Client.

```ruby
priceBooks = client.price_books
```

### <a name="list_price_books"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBooksController.list_price_books") list_price_books

> Returns a paginated list of price books


```ruby
def list_price_books; end
```

#### Example Usage

```ruby

result = priceBooks.list_price_books()

```


### <a name="create_a_price_book"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBooksController.create_a_price_book") create_a_price_book

> Creates a new price book.


```ruby
def create_a_price_book(body); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body_value = "{  \"name\": \"Test\",  \"valid_from\": \"2018-01-01\",  \"valid_to\": \"2019-01-01\",  \"restrict_to_platform_key\": \"1\",  \"customer_group_id\": \"b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4\",  \"outlet_id\": \"\"}";
body = JSON.parse(body_value);

result = priceBooks.create_a_price_book(body)

```


### <a name="get_a_single_price_book"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBooksController.get_a_single_price_book") get_a_single_price_book

> Returns a single price book with a requested `id`


```ruby
def get_a_single_price_book(price_book_id); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| price_book_id |  ``` Required ```  | Valid price book `id`. |


#### Example Usage

```ruby
price_book_id = UUID.new

result = priceBooks.get_a_single_price_book(price_book_id)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="price_book_products_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PriceBookProductsController") PriceBookProductsController

### Get singleton instance

The singleton instance of the ``` PriceBookProductsController ``` class can be accessed from the API Client.

```ruby
priceBookProducts = client.price_book_products
```

### <a name="list_price_book_products"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBookProductsController.list_price_book_products") list_price_book_products

> Returns a paginated list of price book products.


```ruby
def list_price_book_products; end
```

#### Example Usage

```ruby

result = priceBookProducts.list_price_book_products()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="products_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductsController") ProductsController

### Get singleton instance

The singleton instance of the ``` ProductsController ``` class can be accessed from the API Client.

```ruby
products = client.products
```

### <a name="list_products"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.list_products") list_products

> Returns a paginated list of products.


```ruby
def list_products; end
```

#### Example Usage

```ruby

result = products.list_products()

```


### <a name="get_a_single_product"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.get_a_single_product") get_a_single_product

> Returns a single product object with a given `id`.


```ruby
def get_a_single_product(product_id); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| product_id |  ``` Required ```  | Valid product `id`. |


#### Example Usage

```ruby
product_id = UUID.new

result = products.get_a_single_product(product_id)

```


### <a name="get_inventory_data_for_a_single_product"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.get_inventory_data_for_a_single_product") get_inventory_data_for_a_single_product

> Returns inventory data for a single product in all the outlets.


```ruby
def get_inventory_data_for_a_single_product(product_id); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| product_id |  ``` Required ```  | Valid product `id`. |


#### Example Usage

```ruby
product_id = UUID.new

result = products.get_inventory_data_for_a_single_product(product_id)

```


### <a name="upload_an_image"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.upload_an_image") upload_an_image

> Upload a binary file with an image to be used for a product.


```ruby
def upload_an_image(body,
                        product_id = nil); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| product_id |  ``` Optional ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body = UploadAnImageRequest.new
product_id = 'product_id'

result = products.upload_an_image(body, product_id)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="product_images_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductImagesController") ProductImagesController

### Get singleton instance

The singleton instance of the ``` ProductImagesController ``` class can be accessed from the API Client.

```ruby
productImages = client.product_images
```

### <a name="get_a_single_product_image_data"></a>![Method: ](https://apidocs.io/img/method.png ".ProductImagesController.get_a_single_product_image_data") get_a_single_product_image_data

> Returns the metadata for a single product image with a given `id`.
> This method is useful for checking the status of an image after it was uploaded.


```ruby
def get_a_single_product_image_data(product_image_id); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| product_image_id |  ``` Required ```  | Valid product `id`. |


#### Example Usage

```ruby
product_image_id = UUID.new

result = productImages.get_a_single_product_image_data(product_image_id)

```


### <a name="update_set_image_position"></a>![Method: ](https://apidocs.io/img/method.png ".ProductImagesController.update_set_image_position") update_set_image_position

> Allows for changing the image position in the list


```ruby
def update_set_image_position(body,
                                  product_image_id = nil); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| product_image_id |  ``` Optional ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
body_value = "{  \"position\": 1}";
body = JSON.parse(body_value);
product_image_id = 'product_image_id'

result = productImages.update_set_image_position(body, product_image_id)

```


### <a name="delete_a_product_image"></a>![Method: ](https://apidocs.io/img/method.png ".ProductImagesController.delete_a_product_image") delete_a_product_image

> Deletes the product_image with the requested `id`.


```ruby
def delete_a_product_image(product_image_id = nil); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| product_image_id |  ``` Optional ```  | TODO: Add a parameter description |


#### Example Usage

```ruby
product_image_id = 'product_image_id'

productImages.delete_a_product_image(product_image_id)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="product_types_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductTypesController") ProductTypesController

### Get singleton instance

The singleton instance of the ``` ProductTypesController ``` class can be accessed from the API Client.

```ruby
productTypes = client.product_types
```

### <a name="list_product_types"></a>![Method: ](https://apidocs.io/img/method.png ".ProductTypesController.list_product_types") list_product_types

> Returns a paginated list of product types.


```ruby
def list_product_types; end
```

#### Example Usage

```ruby

result = productTypes.list_product_types()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="registers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".RegistersController") RegistersController

### Get singleton instance

The singleton instance of the ``` RegistersController ``` class can be accessed from the API Client.

```ruby
registers = client.registers
```

### <a name="list_registers"></a>![Method: ](https://apidocs.io/img/method.png ".RegistersController.list_registers") list_registers

> Returns a paginated list of registers.


```ruby
def list_registers; end
```

#### Example Usage

```ruby

result = registers.list_registers()

```


### <a name="get_a_single_register"></a>![Method: ](https://apidocs.io/img/method.png ".RegistersController.get_a_single_register") get_a_single_register

> Returns a single register with the requested `id`.


```ruby
def get_a_single_register(register_id); end
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| register_id |  ``` Required ```  | Valid register `id`. |


#### Example Usage

```ruby
register_id = UUID.new

result = registers.get_a_single_register(register_id)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="tags_controller"></a>![Class: ](https://apidocs.io/img/class.png ".TagsController") TagsController

### Get singleton instance

The singleton instance of the ``` TagsController ``` class can be accessed from the API Client.

```ruby
tags = client.tags
```

### <a name="list_tags"></a>![Method: ](https://apidocs.io/img/method.png ".TagsController.list_tags") list_tags

> Returns a collection of tags.


```ruby
def list_tags; end
```

#### Example Usage

```ruby

result = tags.list_tags()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="sales_controller"></a>![Class: ](https://apidocs.io/img/class.png ".SalesController") SalesController

### Get singleton instance

The singleton instance of the ``` SalesController ``` class can be accessed from the API Client.

```ruby
sales = client.sales
```

### <a name="list_sales"></a>![Method: ](https://apidocs.io/img/method.png ".SalesController.list_sales") list_sales

> Returns a paginated list of Sales.


```ruby
def list_sales; end
```

#### Example Usage

```ruby

result = sales.list_sales()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="suppliers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".SuppliersController") SuppliersController

### Get singleton instance

The singleton instance of the ``` SuppliersController ``` class can be accessed from the API Client.

```ruby
suppliers = client.suppliers
```

### <a name="list_suppliers"></a>![Method: ](https://apidocs.io/img/method.png ".SuppliersController.list_suppliers") list_suppliers

> Returns a paginated list of suppliers.


```ruby
def list_suppliers; end
```

#### Example Usage

```ruby

result = suppliers.list_suppliers()

```


[Back to List of Controllers](#list_of_controllers)



