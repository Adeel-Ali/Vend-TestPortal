# Getting started

TODO: Add a description

## How to Build

The generated code has dependencies over external libraries like UniRest. These dependencies are defined in the ```composer.json``` file that comes with the SDK. 
To resolve these dependencies, we use the Composer package manager which requires PHP greater than 5.3.2 installed in your system. 
Visit [https://getcomposer.org/download/](https://getcomposer.org/download/) to download the installer file for Composer and run it in your system. 
Open command prompt and type ```composer --version```. This should display the current version of the Composer installed if the installation was successful.

* Using command line, navigate to the directory containing the generated files (including ```composer.json```) for the SDK. 
* Run the command ```composer install```. This should install all the required dependencies and create the ```vendor``` directory in your project directory.

![Building SDK - Step 1](https://apidocs.io/illustration/php?step=installDependencies&workspaceFolder=Vend%20REST%20API%202.0-PHP)

### [For Windows Users Only] Configuring CURL Certificate Path in php.ini

CURL used to include a list of accepted CAs, but no longer bundles ANY CA certs. So by default it will reject all SSL certificates as unverifiable. You will have to get your CA's cert and point curl at it. The steps are as follows:

1. Download the certificate bundle (.pem file) from [https://curl.haxx.se/docs/caextract.html](https://curl.haxx.se/docs/caextract.html) on to your system.
2. Add curl.cainfo = "PATH_TO/cacert.pem" to your php.ini file located in your php installation. “PATH_TO” must be an absolute path containing the .pem file.

```ini
[curl]
; A default value for the CURLOPT_CAINFO option. This is required to be an
; absolute path.
;curl.cainfo =
```

## How to Use

The following section explains how to use the VendRESTAPI20 library in a new project.

### 1. Open Project in an IDE

Open an IDE for PHP like PhpStorm. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

![Open project in PHPStorm - Step 1](https://apidocs.io/illustration/php?step=openIDE&workspaceFolder=Vend%20REST%20API%202.0-PHP)

Click on ```Open``` in PhpStorm to browse to your generated SDK directory and then click ```OK```.

![Open project in PHPStorm - Step 2](https://apidocs.io/illustration/php?step=openProject0&workspaceFolder=Vend%20REST%20API%202.0-PHP)     

### 2. Add a new Test Project

Create a new directory by right clicking on the solution name as shown below:

![Add a new project in PHPStorm - Step 1](https://apidocs.io/illustration/php?step=createDirectory&workspaceFolder=Vend%20REST%20API%202.0-PHP)

Name the directory as "test"

![Add a new project in PHPStorm - Step 2](https://apidocs.io/illustration/php?step=nameDirectory&workspaceFolder=Vend%20REST%20API%202.0-PHP)
   
Add a PHP file to this project

![Add a new project in PHPStorm - Step 3](https://apidocs.io/illustration/php?step=createFile&workspaceFolder=Vend%20REST%20API%202.0-PHP)

Name it "testSDK"

![Add a new project in PHPStorm - Step 4](https://apidocs.io/illustration/php?step=nameFile&workspaceFolder=Vend%20REST%20API%202.0-PHP)

Depending on your project setup, you might need to include composer's autoloader in your PHP code to enable auto loading of classes.

```PHP
require_once "../vendor/autoload.php";
```

It is important that the path inside require_once correctly points to the file ```autoload.php``` inside the vendor directory created during dependency installations.

![Add a new project in PHPStorm - Step 4](https://apidocs.io/illustration/php?step=projectFiles&workspaceFolder=Vend%20REST%20API%202.0-PHP)

After this you can add code to initialize the client library and acquire the instance of a Controller class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

### 3. Run the Test Project

To run your project you must set the Interpreter for your project. Interpreter is the PHP engine installed on your computer.

Open ```Settings``` from ```File``` menu.

![Run Test Project - Step 1](https://apidocs.io/illustration/php?step=openSettings&workspaceFolder=Vend%20REST%20API%202.0-PHP)

Select ```PHP``` from within ```Languages & Frameworks```

![Run Test Project - Step 2](https://apidocs.io/illustration/php?step=setInterpreter0&workspaceFolder=Vend%20REST%20API%202.0-PHP)

Browse for Interpreters near the ```Interpreter``` option and choose your interpreter.

![Run Test Project - Step 3](https://apidocs.io/illustration/php?step=setInterpreter1&workspaceFolder=Vend%20REST%20API%202.0-PHP)

Once the interpreter is selected, click ```OK```

![Run Test Project - Step 4](https://apidocs.io/illustration/php?step=setInterpreter2&workspaceFolder=Vend%20REST%20API%202.0-PHP)

To run your project, right click on your PHP file inside your Test project and click on ```Run```

![Run Test Project - Step 5](https://apidocs.io/illustration/php?step=runProject&workspaceFolder=Vend%20REST%20API%202.0-PHP)

## How to Test

Unit tests in this SDK can be run using PHPUnit. 

1. First install the dependencies using composer including the `require-dev` dependencies.
2. Run `vendor\bin\phpunit --verbose` from commandline to execute tests. If you have 
   installed PHPUnit globally, run tests using `phpunit --verbose` instead.

You can change the PHPUnit test configuration in the `phpunit.xml` file.

## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| oAuthAccessToken | OAuth 2.0 Access Token |



API client can be initialized as following.

```php
$oAuthAccessToken = 'oAuthAccessToken'; // OAuth 2.0 Access Token

$client = new VendRESTAPI20Lib\VendRESTAPI20Client($oAuthAccessToken);
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

### Get singleton instance

The singleton instance of the ``` BrandsController ``` class can be accessed from the API Client.

```php
$brands = $client->getBrands();
```

### <a name="list_brands"></a>![Method: ](https://apidocs.io/img/method.png ".BrandsController.listBrands") listBrands

> Returns a paginated list of brands.


```php
function listBrands()
```

#### Example Usage

```php

$result = $brands->listBrands();

```


[Back to List of Controllers](#list_of_controllers)

## <a name="customers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CustomersController") CustomersController

### Get singleton instance

The singleton instance of the ``` CustomersController ``` class can be accessed from the API Client.

```php
$customers = $client->getCustomers();
```

### <a name="list_customers"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.listCustomers") listCustomers

> Returns a paginated list of customers.


```php
function listCustomers()
```

#### Example Usage

```php

$result = $customers->listCustomers();

```


### <a name="create_a_new_customer"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.createANewCustomer") createANewCustomer

> Creates a new customer.


```php
function createANewCustomer($body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$bodyValue = "{  \"customer_code\": \"Tony-QKG3\",  \"customer_group_id\": \"b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4\",  \"enable_loyalty\": true,  \"first_name\": \"Tony\",  \"last_name\": \"Stark\",  \"email\": \"ironman@avengers.com\",  \"note\": \"\",  \"gender\": \"M\",  \"date_of_birth\": \"1963-03-03\",  \"company_name\": \"Stark Inc.\",  \"phone\": \"\",  \"mobile\": \"\",  \"fax\": \"\",  \"twitter\": \"\",  \"website\": \"\",  \"physical_address_1\": \"\",  \"physical_address_2\": \"\",  \"physical_suburb\": \"\",  \"physical_city\": \"\",  \"physical_postcode\": \"\",  \"physical_state\": \"\",  \"physical_country_id\": \"US\",  \"postal_address_1\": \"\",  \"postal_address_2\": \"\",  \"postal_suburb\": \"\",  \"postal_city\": \"\",  \"postal_postcode\": \"\",  \"postal_state\": \"\",  \"postal_country_id\": \"\",  \"custom_field_1\": \"\",  \"custom_field_2\": \"\",  \"custom_field_3\": \"\",  \"custom_field_4\": \"\"}";
$body = APIHelper::deserialize($bodyValue);

$result = $customers->createANewCustomer($body);

```


### <a name="get_a_single_customer"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.getASingleCustomer") getASingleCustomer

> Returns a single customer with a requested `id`.


```php
function getASingleCustomer($customerId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |



#### Example Usage

```php
$customerId = uniqid();

$result = $customers->getASingleCustomer($customerId);

```


### <a name="update_a_customer"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.updateACustomer") updateACustomer

> Updates editable fields for the customer with the requested `id`.


```php
function updateACustomer(
        $customerId,
        $body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$customerId = uniqid();
$body = new CustomerBase();

$result = $customers->updateACustomer($customerId, $body);

```


### <a name="delete_a_customer"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.deleteACustomer") deleteACustomer

> Deletes the customer with the requested `id`.


```php
function deleteACustomer($customerId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |



#### Example Usage

```php
$customerId = uniqid();

$customers->deleteACustomer($customerId);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="customer_groups_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CustomerGroupsController") CustomerGroupsController

### Get singleton instance

The singleton instance of the ``` CustomerGroupsController ``` class can be accessed from the API Client.

```php
$customerGroups = $client->getCustomerGroups();
```

### <a name="list_customer_groups"></a>![Method: ](https://apidocs.io/img/method.png ".CustomerGroupsController.listCustomerGroups") listCustomerGroups

> Returns a paginated list of customer groups.


```php
function listCustomerGroups()
```

#### Example Usage

```php

$result = $customerGroups->listCustomerGroups();

```


[Back to List of Controllers](#list_of_controllers)

## <a name="consignments_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ConsignmentsController") ConsignmentsController

### Get singleton instance

The singleton instance of the ``` ConsignmentsController ``` class can be accessed from the API Client.

```php
$consignments = $client->getConsignments();
```

### <a name="list_consignments"></a>![Method: ](https://apidocs.io/img/method.png ".ConsignmentsController.listConsignments") listConsignments

> Returns a paginated list of consignments.


```php
function listConsignments()
```

#### Example Usage

```php

$result = $consignments->listConsignments();

```


### <a name="get_a_single_consignment"></a>![Method: ](https://apidocs.io/img/method.png ".ConsignmentsController.getASingleConsignment") getASingleConsignment

> Returns a single consignment with the requested `id`.


```php
function getASingleConsignment($consignmentId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| consignmentId |  ``` Required ```  | Valid consignment `id`. |



#### Example Usage

```php
$consignmentId = uniqid();

$result = $consignments->getASingleConsignment($consignmentId);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="inventory_controller"></a>![Class: ](https://apidocs.io/img/class.png ".InventoryController") InventoryController

### Get singleton instance

The singleton instance of the ``` InventoryController ``` class can be accessed from the API Client.

```php
$inventory = $client->getInventory();
```

### <a name="list_inventory_records"></a>![Method: ](https://apidocs.io/img/method.png ".InventoryController.listInventoryRecords") listInventoryRecords

> Returns a paginated list of Inventory records.


```php
function listInventoryRecords()
```

#### Example Usage

```php

$result = $inventory->listInventoryRecords();

```


[Back to List of Controllers](#list_of_controllers)

## <a name="outlets_controller"></a>![Class: ](https://apidocs.io/img/class.png ".OutletsController") OutletsController

### Get singleton instance

The singleton instance of the ``` OutletsController ``` class can be accessed from the API Client.

```php
$outlets = $client->getOutlets();
```

### <a name="list_outlets"></a>![Method: ](https://apidocs.io/img/method.png ".OutletsController.listOutlets") listOutlets

> Returns a collection of outlets.


```php
function listOutlets()
```

#### Example Usage

```php

$result = $outlets->listOutlets();

```


### <a name="get_a_single_outlet"></a>![Method: ](https://apidocs.io/img/method.png ".OutletsController.getASingleOutlet") getASingleOutlet

> Returns a single outlet with the requested `id`.


```php
function getASingleOutlet($outletId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| outletId |  ``` Required ```  | Valid Outlet `id`. |



#### Example Usage

```php
$outletId = uniqid();

$result = $outlets->getASingleOutlet($outletId);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="price_books_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PriceBooksController") PriceBooksController

### Get singleton instance

The singleton instance of the ``` PriceBooksController ``` class can be accessed from the API Client.

```php
$priceBooks = $client->getPriceBooks();
```

### <a name="list_price_books"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBooksController.listPriceBooks") listPriceBooks

> Returns a paginated list of price books


```php
function listPriceBooks()
```

#### Example Usage

```php

$result = $priceBooks->listPriceBooks();

```


### <a name="create_a_price_book"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBooksController.createAPriceBook") createAPriceBook

> Creates a new price book.


```php
function createAPriceBook($body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```php
$bodyValue = "{  \"name\": \"Test\",  \"valid_from\": \"2018-01-01\",  \"valid_to\": \"2019-01-01\",  \"restrict_to_platform_key\": \"1\",  \"customer_group_id\": \"b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4\",  \"outlet_id\": \"\"}";
$body = APIHelper::deserialize($bodyValue);

$result = $priceBooks->createAPriceBook($body);

```


### <a name="get_a_single_price_book"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBooksController.getASinglePriceBook") getASinglePriceBook

> Returns a single price book with a requested `id`


```php
function getASinglePriceBook($priceBookId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| priceBookId |  ``` Required ```  | Valid price book `id`. |



#### Example Usage

```php
$priceBookId = uniqid();

$result = $priceBooks->getASinglePriceBook($priceBookId);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="price_book_products_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PriceBookProductsController") PriceBookProductsController

### Get singleton instance

The singleton instance of the ``` PriceBookProductsController ``` class can be accessed from the API Client.

```php
$priceBookProducts = $client->getPriceBookProducts();
```

### <a name="list_price_book_products"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBookProductsController.listPriceBookProducts") listPriceBookProducts

> Returns a paginated list of price book products.


```php
function listPriceBookProducts()
```

#### Example Usage

```php

$result = $priceBookProducts->listPriceBookProducts();

```


[Back to List of Controllers](#list_of_controllers)

## <a name="products_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductsController") ProductsController

### Get singleton instance

The singleton instance of the ``` ProductsController ``` class can be accessed from the API Client.

```php
$products = $client->getProducts();
```

### <a name="list_products"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.listProducts") listProducts

> Returns a paginated list of products.


```php
function listProducts()
```

#### Example Usage

```php

$result = $products->listProducts();

```


### <a name="get_a_single_product"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.getASingleProduct") getASingleProduct

> Returns a single product object with a given `id`.


```php
function getASingleProduct($productId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productId |  ``` Required ```  | Valid product `id`. |



#### Example Usage

```php
$productId = uniqid();

$result = $products->getASingleProduct($productId);

```


### <a name="get_inventory_data_for_a_single_product"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.getInventoryDataForASingleProduct") getInventoryDataForASingleProduct

> Returns inventory data for a single product in all the outlets.


```php
function getInventoryDataForASingleProduct($productId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productId |  ``` Required ```  | Valid product `id`. |



#### Example Usage

```php
$productId = uniqid();

$result = $products->getInventoryDataForASingleProduct($productId);

```


### <a name="upload_an_image"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.uploadAnImage") uploadAnImage

> Upload a binary file with an image to be used for a product.


```php
function uploadAnImage(
        $body,
        $productId = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| productId |  ``` Optional ```  | TODO: Add a parameter description |



#### Example Usage

```php
$body = new UploadAnImageRequest();
$productId = 'product_id';

$result = $products->uploadAnImage($body, $productId);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="product_images_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductImagesController") ProductImagesController

### Get singleton instance

The singleton instance of the ``` ProductImagesController ``` class can be accessed from the API Client.

```php
$productImages = $client->getProductImages();
```

### <a name="get_a_single_product_image_data"></a>![Method: ](https://apidocs.io/img/method.png ".ProductImagesController.getASingleProductImageData") getASingleProductImageData

> Returns the metadata for a single product image with a given `id`.
> This method is useful for checking the status of an image after it was uploaded.


```php
function getASingleProductImageData($productImageId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productImageId |  ``` Required ```  | Valid product `id`. |



#### Example Usage

```php
$productImageId = uniqid();

$result = $productImages->getASingleProductImageData($productImageId);

```


### <a name="update_set_image_position"></a>![Method: ](https://apidocs.io/img/method.png ".ProductImagesController.updateSetImagePosition") updateSetImagePosition

> Allows for changing the image position in the list


```php
function updateSetImagePosition(
        $body,
        $productImageId = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| productImageId |  ``` Optional ```  | TODO: Add a parameter description |



#### Example Usage

```php
$bodyValue = "{  \"position\": 1}";
$body = APIHelper::deserialize($bodyValue);
$productImageId = 'product_image_id';

$result = $productImages->updateSetImagePosition($body, $productImageId);

```


### <a name="delete_a_product_image"></a>![Method: ](https://apidocs.io/img/method.png ".ProductImagesController.deleteAProductImage") deleteAProductImage

> Deletes the product_image with the requested `id`.


```php
function deleteAProductImage($productImageId = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productImageId |  ``` Optional ```  | TODO: Add a parameter description |



#### Example Usage

```php
$productImageId = 'product_image_id';

$productImages->deleteAProductImage($productImageId);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="product_types_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductTypesController") ProductTypesController

### Get singleton instance

The singleton instance of the ``` ProductTypesController ``` class can be accessed from the API Client.

```php
$productTypes = $client->getProductTypes();
```

### <a name="list_product_types"></a>![Method: ](https://apidocs.io/img/method.png ".ProductTypesController.listProductTypes") listProductTypes

> Returns a paginated list of product types.


```php
function listProductTypes()
```

#### Example Usage

```php

$result = $productTypes->listProductTypes();

```


[Back to List of Controllers](#list_of_controllers)

## <a name="registers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".RegistersController") RegistersController

### Get singleton instance

The singleton instance of the ``` RegistersController ``` class can be accessed from the API Client.

```php
$registers = $client->getRegisters();
```

### <a name="list_registers"></a>![Method: ](https://apidocs.io/img/method.png ".RegistersController.listRegisters") listRegisters

> Returns a paginated list of registers.


```php
function listRegisters()
```

#### Example Usage

```php

$result = $registers->listRegisters();

```


### <a name="get_a_single_register"></a>![Method: ](https://apidocs.io/img/method.png ".RegistersController.getASingleRegister") getASingleRegister

> Returns a single register with the requested `id`.


```php
function getASingleRegister($registerId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| registerId |  ``` Required ```  | Valid register `id`. |



#### Example Usage

```php
$registerId = uniqid();

$result = $registers->getASingleRegister($registerId);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="tags_controller"></a>![Class: ](https://apidocs.io/img/class.png ".TagsController") TagsController

### Get singleton instance

The singleton instance of the ``` TagsController ``` class can be accessed from the API Client.

```php
$tags = $client->getTags();
```

### <a name="list_tags"></a>![Method: ](https://apidocs.io/img/method.png ".TagsController.listTags") listTags

> Returns a collection of tags.


```php
function listTags()
```

#### Example Usage

```php

$result = $tags->listTags();

```


[Back to List of Controllers](#list_of_controllers)

## <a name="sales_controller"></a>![Class: ](https://apidocs.io/img/class.png ".SalesController") SalesController

### Get singleton instance

The singleton instance of the ``` SalesController ``` class can be accessed from the API Client.

```php
$sales = $client->getSales();
```

### <a name="list_sales"></a>![Method: ](https://apidocs.io/img/method.png ".SalesController.listSales") listSales

> Returns a paginated list of Sales.


```php
function listSales()
```

#### Example Usage

```php

$result = $sales->listSales();

```


[Back to List of Controllers](#list_of_controllers)

## <a name="suppliers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".SuppliersController") SuppliersController

### Get singleton instance

The singleton instance of the ``` SuppliersController ``` class can be accessed from the API Client.

```php
$suppliers = $client->getSuppliers();
```

### <a name="list_suppliers"></a>![Method: ](https://apidocs.io/img/method.png ".SuppliersController.listSuppliers") listSuppliers

> Returns a paginated list of suppliers.


```php
function listSuppliers()
```

#### Example Usage

```php

$result = $suppliers->listSuppliers();

```


[Back to List of Controllers](#list_of_controllers)



