# Getting started

TODO: Add a description

## How to Build


You must have Python 2 >=2.7.9 or Python 3 >=3.4 installed on your system to install and run this SDK. This SDK package depends on other Python packages like nose, jsonpickle etc. 
These dependencies are defined in the ```requirements.txt``` file that comes with the SDK.
To resolve these dependencies, you can use the PIP Dependency manager. Install it by following steps at [https://pip.pypa.io/en/stable/installing/](https://pip.pypa.io/en/stable/installing/).

Python and PIP executables should be defined in your PATH. Open command prompt and type ```pip --version```.
This should display the version of the PIP Dependency Manager installed if your installation was successful and the paths are properly defined.

* Using command line, navigate to the directory containing the generated files (including ```requirements.txt```) for the SDK.
* Run the command ```pip install -r requirements.txt```. This should install all the required dependencies.

![Building SDK - Step 1](https://apidocs.io/illustration/python?step=installDependencies&workspaceFolder=Vend%20REST%20API%202.0-Python)


## How to Use

The following section explains how to use the Vendrestapi20 SDK package in a new project.

### 1. Open Project in an IDE

Open up a Python IDE like PyCharm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PyCharm - Step 1](https://apidocs.io/illustration/python?step=pyCharm)

Click on ```Open``` in PyCharm to browse to your generated SDK directory and then click ```OK```.

![Open project in PyCharm - Step 2](https://apidocs.io/illustration/python?step=openProject0&workspaceFolder=Vend%20REST%20API%202.0-Python)     

The project files will be displayed in the side bar as follows:

![Open project in PyCharm - Step 3](https://apidocs.io/illustration/python?step=openProject1&workspaceFolder=Vend%20REST%20API%202.0-Python&projectName=vendrestapi20)     

### 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PyCharm - Step 1](https://apidocs.io/illustration/python?step=createDirectory&workspaceFolder=Vend%20REST%20API%202.0-Python&projectName=vendrestapi20)

Name the directory as "test"

![Add a new project in PyCharm - Step 2](https://apidocs.io/illustration/python?step=nameDirectory)
   
Add a python file to this project with the name "testsdk"

![Add a new project in PyCharm - Step 3](https://apidocs.io/illustration/python?step=createFile&workspaceFolder=Vend%20REST%20API%202.0-Python&projectName=vendrestapi20)

Name it "testsdk"

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?step=nameFile)

In your python file you will be required to import the generated python library using the following code lines

```Python
from vendrestapi20.vendrestapi_20_client import Vendrestapi20Client
```

![Add a new project in PyCharm - Step 4](https://apidocs.io/illustration/python?step=projectFiles&workspaceFolder=Vend%20REST%20API%202.0-Python&libraryName=vendrestapi20.vendrestapi_20_client&projectName=vendrestapi20)

After this you can write code to instantiate an API client object, get a controller object and  make API calls. Sample code is given in the subsequent sections.

### 3. Run the Test Project

To run the file within your test project, right click on your Python file inside your Test project and click on ```Run```

![Run Test Project - Step 1](https://apidocs.io/illustration/python?step=runProject&workspaceFolder=Vend%20REST%20API%202.0-Python&libraryName=vendrestapi20.vendrestapi_20_client&projectName=vendrestapi20)


## How to Test

You can test the generated SDK and the server with automatically generated test
cases. unittest is used as the testing framework and nose is used as the test
runner. You can run the tests as follows:

  1. From terminal/cmd navigate to the root directory of the SDK.
  2. Invoke 'pip install -r test-requirements.txt'
  3. Invoke 'nosetests'

## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| o_auth_access_token | OAuth 2.0 Access Token |



API client can be initialized as following.

```python
# Configuration parameters and credentials
o_auth_access_token = 'o_auth_access_token' # OAuth 2.0 Access Token

client = Vendrestapi20Client(o_auth_access_token)
```



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

### Get controller instance

An instance of the ``` BrandsController ``` class can be accessed from the API Client.

```python
 brands_client = client.brands
```

### <a name="list_brands"></a>![Method: ](https://apidocs.io/img/method.png ".BrandsController.list_brands") list_brands

> Returns a paginated list of brands.

```python
def list_brands(self)
```

#### Example Usage

```python

result = brands_client.list_brands()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="customers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CustomersController") CustomersController

### Get controller instance

An instance of the ``` CustomersController ``` class can be accessed from the API Client.

```python
 customers_client = client.customers
```

### <a name="list_customers"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.list_customers") list_customers

> Returns a paginated list of customers.

```python
def list_customers(self)
```

#### Example Usage

```python

result = customers_client.list_customers()

```


### <a name="create_a_new_customer"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.create_a_new_customer") create_a_new_customer

> Creates a new customer.

```python
def create_a_new_customer(self,
                              body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body_value = "{  \"customer_code\": \"Tony-QKG3\",  \"customer_group_id\": \"b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4\",  \"enable_loyalty\": true,  \"first_name\": \"Tony\",  \"last_name\": \"Stark\",  \"email\": \"ironman@avengers.com\",  \"note\": \"\",  \"gender\": \"M\",  \"date_of_birth\": \"1963-03-03\",  \"company_name\": \"Stark Inc.\",  \"phone\": \"\",  \"mobile\": \"\",  \"fax\": \"\",  \"twitter\": \"\",  \"website\": \"\",  \"physical_address_1\": \"\",  \"physical_address_2\": \"\",  \"physical_suburb\": \"\",  \"physical_city\": \"\",  \"physical_postcode\": \"\",  \"physical_state\": \"\",  \"physical_country_id\": \"US\",  \"postal_address_1\": \"\",  \"postal_address_2\": \"\",  \"postal_suburb\": \"\",  \"postal_city\": \"\",  \"postal_postcode\": \"\",  \"postal_state\": \"\",  \"postal_country_id\": \"\",  \"custom_field_1\": \"\",  \"custom_field_2\": \"\",  \"custom_field_3\": \"\",  \"custom_field_4\": \"\"}"
body = json.loads(body_value)

result = customers_client.create_a_new_customer(body)

```


### <a name="get_a_single_customer"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.get_a_single_customer") get_a_single_customer

> Returns a single customer with a requested `id`.

```python
def get_a_single_customer(self,
                              customer_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |



#### Example Usage

```python
customer_id = uuid.uuid4()

result = customers_client.get_a_single_customer(customer_id)

```


### <a name="update_a_customer"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.update_a_customer") update_a_customer

> Updates editable fields for the customer with the requested `id`.

```python
def update_a_customer(self,
                          customer_id,
                          body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
customer_id = uuid.uuid4()
body = CustomerBase()

result = customers_client.update_a_customer(customer_id, body)

```


### <a name="delete_a_customer"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.delete_a_customer") delete_a_customer

> Deletes the customer with the requested `id`.

```python
def delete_a_customer(self,
                          customer_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |



#### Example Usage

```python
customer_id = uuid.uuid4()

customers_client.delete_a_customer(customer_id)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="customer_groups_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CustomerGroupsController") CustomerGroupsController

### Get controller instance

An instance of the ``` CustomerGroupsController ``` class can be accessed from the API Client.

```python
 customer_groups_client = client.customer_groups
```

### <a name="list_customer_groups"></a>![Method: ](https://apidocs.io/img/method.png ".CustomerGroupsController.list_customer_groups") list_customer_groups

> Returns a paginated list of customer groups.

```python
def list_customer_groups(self)
```

#### Example Usage

```python

result = customer_groups_client.list_customer_groups()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="consignments_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ConsignmentsController") ConsignmentsController

### Get controller instance

An instance of the ``` ConsignmentsController ``` class can be accessed from the API Client.

```python
 consignments_client = client.consignments
```

### <a name="list_consignments"></a>![Method: ](https://apidocs.io/img/method.png ".ConsignmentsController.list_consignments") list_consignments

> Returns a paginated list of consignments.

```python
def list_consignments(self)
```

#### Example Usage

```python

result = consignments_client.list_consignments()

```


### <a name="get_a_single_consignment"></a>![Method: ](https://apidocs.io/img/method.png ".ConsignmentsController.get_a_single_consignment") get_a_single_consignment

> Returns a single consignment with the requested `id`.

```python
def get_a_single_consignment(self,
                                 consignment_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| consignmentId |  ``` Required ```  | Valid consignment `id`. |



#### Example Usage

```python
consignment_id = uuid.uuid4()

result = consignments_client.get_a_single_consignment(consignment_id)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="inventory_controller"></a>![Class: ](https://apidocs.io/img/class.png ".InventoryController") InventoryController

### Get controller instance

An instance of the ``` InventoryController ``` class can be accessed from the API Client.

```python
 inventory_client = client.inventory
```

### <a name="list_inventory_records"></a>![Method: ](https://apidocs.io/img/method.png ".InventoryController.list_inventory_records") list_inventory_records

> Returns a paginated list of Inventory records.

```python
def list_inventory_records(self)
```

#### Example Usage

```python

result = inventory_client.list_inventory_records()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="outlets_controller"></a>![Class: ](https://apidocs.io/img/class.png ".OutletsController") OutletsController

### Get controller instance

An instance of the ``` OutletsController ``` class can be accessed from the API Client.

```python
 outlets_client = client.outlets
```

### <a name="list_outlets"></a>![Method: ](https://apidocs.io/img/method.png ".OutletsController.list_outlets") list_outlets

> Returns a collection of outlets.

```python
def list_outlets(self)
```

#### Example Usage

```python

result = outlets_client.list_outlets()

```


### <a name="get_a_single_outlet"></a>![Method: ](https://apidocs.io/img/method.png ".OutletsController.get_a_single_outlet") get_a_single_outlet

> Returns a single outlet with the requested `id`.

```python
def get_a_single_outlet(self,
                            outlet_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| outletId |  ``` Required ```  | Valid Outlet `id`. |



#### Example Usage

```python
outlet_id = uuid.uuid4()

result = outlets_client.get_a_single_outlet(outlet_id)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="price_books_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PriceBooksController") PriceBooksController

### Get controller instance

An instance of the ``` PriceBooksController ``` class can be accessed from the API Client.

```python
 price_books_client = client.price_books
```

### <a name="list_price_books"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBooksController.list_price_books") list_price_books

> Returns a paginated list of price books

```python
def list_price_books(self)
```

#### Example Usage

```python

result = price_books_client.list_price_books()

```


### <a name="create_a_price_book"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBooksController.create_a_price_book") create_a_price_book

> Creates a new price book.

```python
def create_a_price_book(self,
                            body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```python
body_value = "{  \"name\": \"Test\",  \"valid_from\": \"2018-01-01\",  \"valid_to\": \"2019-01-01\",  \"restrict_to_platform_key\": \"1\",  \"customer_group_id\": \"b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4\",  \"outlet_id\": \"\"}"
body = json.loads(body_value)

result = price_books_client.create_a_price_book(body)

```


### <a name="get_a_single_price_book"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBooksController.get_a_single_price_book") get_a_single_price_book

> Returns a single price book with a requested `id`

```python
def get_a_single_price_book(self,
                                price_book_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| priceBookId |  ``` Required ```  | Valid price book `id`. |



#### Example Usage

```python
price_book_id = uuid.uuid4()

result = price_books_client.get_a_single_price_book(price_book_id)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="price_book_products_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PriceBookProductsController") PriceBookProductsController

### Get controller instance

An instance of the ``` PriceBookProductsController ``` class can be accessed from the API Client.

```python
 price_book_products_client = client.price_book_products
```

### <a name="list_price_book_products"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBookProductsController.list_price_book_products") list_price_book_products

> Returns a paginated list of price book products.

```python
def list_price_book_products(self)
```

#### Example Usage

```python

result = price_book_products_client.list_price_book_products()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="products_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductsController") ProductsController

### Get controller instance

An instance of the ``` ProductsController ``` class can be accessed from the API Client.

```python
 products_client = client.products
```

### <a name="list_products"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.list_products") list_products

> Returns a paginated list of products.

```python
def list_products(self)
```

#### Example Usage

```python

result = products_client.list_products()

```


### <a name="get_a_single_product"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.get_a_single_product") get_a_single_product

> Returns a single product object with a given `id`.

```python
def get_a_single_product(self,
                             product_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productId |  ``` Required ```  | Valid product `id`. |



#### Example Usage

```python
product_id = uuid.uuid4()

result = products_client.get_a_single_product(product_id)

```


### <a name="get_inventory_data_for_a_single_product"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.get_inventory_data_for_a_single_product") get_inventory_data_for_a_single_product

> Returns inventory data for a single product in all the outlets.

```python
def get_inventory_data_for_a_single_product(self,
                                                product_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productId |  ``` Required ```  | Valid product `id`. |



#### Example Usage

```python
product_id = uuid.uuid4()

result = products_client.get_inventory_data_for_a_single_product(product_id)

```


### <a name="upload_an_image"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.upload_an_image") upload_an_image

> Upload a binary file with an image to be used for a product.

```python
def upload_an_image(self,
                        body,
                        product_id=None)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| productId |  ``` Optional ```  | TODO: Add a parameter description |



#### Example Usage

```python
body = UploadAnImageRequest()
product_id = 'product_id'

result = products_client.upload_an_image(body, product_id)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="product_images_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductImagesController") ProductImagesController

### Get controller instance

An instance of the ``` ProductImagesController ``` class can be accessed from the API Client.

```python
 product_images_client = client.product_images
```

### <a name="get_a_single_product_image_data"></a>![Method: ](https://apidocs.io/img/method.png ".ProductImagesController.get_a_single_product_image_data") get_a_single_product_image_data

> Returns the metadata for a single product image with a given `id`.
> This method is useful for checking the status of an image after it was uploaded.

```python
def get_a_single_product_image_data(self,
                                        product_image_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productImageId |  ``` Required ```  | Valid product `id`. |



#### Example Usage

```python
product_image_id = uuid.uuid4()

result = product_images_client.get_a_single_product_image_data(product_image_id)

```


### <a name="update_set_image_position"></a>![Method: ](https://apidocs.io/img/method.png ".ProductImagesController.update_set_image_position") update_set_image_position

> Allows for changing the image position in the list

```python
def update_set_image_position(self,
                                  body,
                                  product_image_id=None)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| productImageId |  ``` Optional ```  | TODO: Add a parameter description |



#### Example Usage

```python
body_value = "{  \"position\": 1}"
body = json.loads(body_value)
product_image_id = 'product_image_id'

result = product_images_client.update_set_image_position(body, product_image_id)

```


### <a name="delete_a_product_image"></a>![Method: ](https://apidocs.io/img/method.png ".ProductImagesController.delete_a_product_image") delete_a_product_image

> Deletes the product_image with the requested `id`.

```python
def delete_a_product_image(self,
                               product_image_id=None)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productImageId |  ``` Optional ```  | TODO: Add a parameter description |



#### Example Usage

```python
product_image_id = 'product_image_id'

product_images_client.delete_a_product_image(product_image_id)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="product_types_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductTypesController") ProductTypesController

### Get controller instance

An instance of the ``` ProductTypesController ``` class can be accessed from the API Client.

```python
 product_types_client = client.product_types
```

### <a name="list_product_types"></a>![Method: ](https://apidocs.io/img/method.png ".ProductTypesController.list_product_types") list_product_types

> Returns a paginated list of product types.

```python
def list_product_types(self)
```

#### Example Usage

```python

result = product_types_client.list_product_types()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="registers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".RegistersController") RegistersController

### Get controller instance

An instance of the ``` RegistersController ``` class can be accessed from the API Client.

```python
 registers_client = client.registers
```

### <a name="list_registers"></a>![Method: ](https://apidocs.io/img/method.png ".RegistersController.list_registers") list_registers

> Returns a paginated list of registers.

```python
def list_registers(self)
```

#### Example Usage

```python

result = registers_client.list_registers()

```


### <a name="get_a_single_register"></a>![Method: ](https://apidocs.io/img/method.png ".RegistersController.get_a_single_register") get_a_single_register

> Returns a single register with the requested `id`.

```python
def get_a_single_register(self,
                              register_id)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| registerId |  ``` Required ```  | Valid register `id`. |



#### Example Usage

```python
register_id = uuid.uuid4()

result = registers_client.get_a_single_register(register_id)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="tags_controller"></a>![Class: ](https://apidocs.io/img/class.png ".TagsController") TagsController

### Get controller instance

An instance of the ``` TagsController ``` class can be accessed from the API Client.

```python
 tags_client = client.tags
```

### <a name="list_tags"></a>![Method: ](https://apidocs.io/img/method.png ".TagsController.list_tags") list_tags

> Returns a collection of tags.

```python
def list_tags(self)
```

#### Example Usage

```python

result = tags_client.list_tags()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="sales_controller"></a>![Class: ](https://apidocs.io/img/class.png ".SalesController") SalesController

### Get controller instance

An instance of the ``` SalesController ``` class can be accessed from the API Client.

```python
 sales_client = client.sales
```

### <a name="list_sales"></a>![Method: ](https://apidocs.io/img/method.png ".SalesController.list_sales") list_sales

> Returns a paginated list of Sales.

```python
def list_sales(self)
```

#### Example Usage

```python

result = sales_client.list_sales()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="suppliers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".SuppliersController") SuppliersController

### Get controller instance

An instance of the ``` SuppliersController ``` class can be accessed from the API Client.

```python
 suppliers_client = client.suppliers
```

### <a name="list_suppliers"></a>![Method: ](https://apidocs.io/img/method.png ".SuppliersController.list_suppliers") list_suppliers

> Returns a paginated list of suppliers.

```python
def list_suppliers(self)
```

#### Example Usage

```python

result = suppliers_client.list_suppliers()

```


[Back to List of Controllers](#list_of_controllers)



