# Getting started

TODO: Add a description

## How to Build

The generated SDK relies on [Node Package Manager](https://www.npmjs.com/) (NPM) being available to resolve dependencies. If you don't already have NPM installed, please go ahead and follow instructions to install NPM from [here](https://nodejs.org/en/download/).
The SDK also requires Node to be installed. If Node isn't already installed, please install it from [here](https://nodejs.org/en/download/)
> NPM is installed by default when Node is installed

To check if node and npm have been successfully installed, write the following commands in command prompt:

* `node --version`
* `npm -version`

![Version Check](https://apidocs.io/illustration/nodejs?step=versionCheck&workspaceFolder=Vend%20REST%20API%202.0-Node)

Now use npm to resolve all dependencies by running the following command in the root directory (of the SDK folder):

```bash
npm install
```

![Resolve Dependencies](https://apidocs.io/illustration/nodejs?step=resolveDependency1&workspaceFolder=Vend%20REST%20API%202.0-Node)

![Resolve Dependencies](https://apidocs.io/illustration/nodejs?step=resolveDependency2)

This will install all dependencies in the `node_modules` folder.

Once dependencies are resolved, you will need to move the folder `VendRESTAPI20Lib ` in to your `node_modules` folder.

## How to Use

The following section explains how to use the library in a new project.

### 1. Open Project Folder
Open an IDE/Text Editor for JavaScript like Sublime Text. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.

Click on `File` and select `Open Folder`.

![Open Folder](https://apidocs.io/illustration/nodejs?step=openFolder)

Select the folder of your SDK and click on `Select Folder` to open it up in Sublime Text. The folder will become visible in the bar on the left.

![Open Project](https://apidocs.io/illustration/nodejs?step=openProject&workspaceFolder=Vend%20REST%20API%202.0-Node)

### 2. Creating a Test File

Now right click on the folder name and select the `New File` option to create a new test file. Save it as `index.js` Now import the generated NodeJS library using the following lines of code:

```js
var lib = require('lib');
```

Save changes.

![Create new file](https://apidocs.io/illustration/nodejs?step=createNewFile&workspaceFolder=Vend%20REST%20API%202.0-Node)

![Save new file](https://apidocs.io/illustration/nodejs?step=saveNewFile&workspaceFolder=Vend%20REST%20API%202.0-Node)

### 3. Running The Test File

To run the `index.js` file, open up the command prompt and navigate to the Path where the SDK folder resides. Type the following command to run the file:

```
node index.js
```

![Run file](https://apidocs.io/illustration/nodejs?step=runProject&workspaceFolder=Vend%20REST%20API%202.0-Node)


## How to Test

These tests use Mocha framework for testing, coupled with Chai for assertions. These dependencies need to be installed for tests to run.
Tests can be run in a number of ways:

### Method 1 (Run all tests)

1. Navigate to the root directory of the SDK folder from command prompt.
2. Type `mocha --recursive` to run all the tests.

### Method 2 (Run all tests)

1. Navigate to the `../test/Controllers/` directory from command prompt.
2. Type `mocha *` to run all the tests.

### Method 3 (Run specific controller's tests)

1. Navigate to the `../test/Controllers/` directory from command prompt.
2. Type `mocha  Vend REST API 2.0Controller`  to run all the tests in that controller file.

> To increase mocha's default timeout, you can change the `TEST_TIMEOUT` parameter's value in `TestBootstrap.js`.

![Run Tests](https://apidocs.io/illustration/nodejs?step=runTests&controllerName=Vend%20REST%20API%202.0Controller)

## Initialization

### Authentication
In order to setup authentication in the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| oAuthAccessToken | OAuth 2.0 Access Token |



API client can be initialized as following:

```JavaScript
const lib = require('lib');

// Configuration parameters and credentials
lib.Configuration.oAuthAccessToken = "oAuthAccessToken"; // OAuth 2.0 Access Token

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

```javascript
var controller = lib.BrandsController;
```

### <a name="list_brands"></a>![Method: ](https://apidocs.io/img/method.png ".BrandsController.listBrands") listBrands

> Returns a paginated list of brands.


```javascript
function listBrands(callback)
```

#### Example Usage

```javascript


    controller.listBrands(function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="customers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CustomersController") CustomersController

### Get singleton instance

The singleton instance of the ``` CustomersController ``` class can be accessed from the API Client.

```javascript
var controller = lib.CustomersController;
```

### <a name="list_customers"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.listCustomers") listCustomers

> Returns a paginated list of customers.


```javascript
function listCustomers(callback)
```

#### Example Usage

```javascript


    controller.listCustomers(function(error, response, context) {

    
    });
```



### <a name="create_a_new_customer"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.createANewCustomer") createANewCustomer

> Creates a new customer.


```javascript
function createANewCustomer(body, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new CustomerBase({  "customer_code": "Tony-QKG3",  "customer_group_id": "b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4",  "enable_loyalty": true,  "first_name": "Tony",  "last_name": "Stark",  "email": "ironman@avengers.com",  "note": "",  "gender": "M",  "date_of_birth": "1963-03-03",  "company_name": "Stark Inc.",  "phone": "",  "mobile": "",  "fax": "",  "twitter": "",  "website": "",  "physical_address_1": "",  "physical_address_2": "",  "physical_suburb": "",  "physical_city": "",  "physical_postcode": "",  "physical_state": "",  "physical_country_id": "US",  "postal_address_1": "",  "postal_address_2": "",  "postal_suburb": "",  "postal_city": "",  "postal_postcode": "",  "postal_state": "",  "postal_country_id": "",  "custom_field_1": "",  "custom_field_2": "",  "custom_field_3": "",  "custom_field_4": ""});

    controller.createANewCustomer(body, function(error, response, context) {

    
    });
```



### <a name="get_a_single_customer"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.getASingleCustomer") getASingleCustomer

> Returns a single customer with a requested `id`.


```javascript
function getASingleCustomer(customerId, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |



#### Example Usage

```javascript

    var customerId = uniqid();

    controller.getASingleCustomer(customerId, function(error, response, context) {

    
    });
```



### <a name="update_a_customer"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.updateACustomer") updateACustomer

> Updates editable fields for the customer with the requested `id`.


```javascript
function updateACustomer(customerId, body, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var customerId = uniqid();
    var body = new CustomerBase({"key":"value"});

    controller.updateACustomer(customerId, body, function(error, response, context) {

    
    });
```



### <a name="delete_a_customer"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.deleteACustomer") deleteACustomer

> Deletes the customer with the requested `id`.


```javascript
function deleteACustomer(customerId, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |



#### Example Usage

```javascript

    var customerId = uniqid();

    controller.deleteACustomer(customerId, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="customer_groups_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CustomerGroupsController") CustomerGroupsController

### Get singleton instance

The singleton instance of the ``` CustomerGroupsController ``` class can be accessed from the API Client.

```javascript
var controller = lib.CustomerGroupsController;
```

### <a name="list_customer_groups"></a>![Method: ](https://apidocs.io/img/method.png ".CustomerGroupsController.listCustomerGroups") listCustomerGroups

> Returns a paginated list of customer groups.


```javascript
function listCustomerGroups(callback)
```

#### Example Usage

```javascript


    controller.listCustomerGroups(function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="consignments_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ConsignmentsController") ConsignmentsController

### Get singleton instance

The singleton instance of the ``` ConsignmentsController ``` class can be accessed from the API Client.

```javascript
var controller = lib.ConsignmentsController;
```

### <a name="list_consignments"></a>![Method: ](https://apidocs.io/img/method.png ".ConsignmentsController.listConsignments") listConsignments

> Returns a paginated list of consignments.


```javascript
function listConsignments(callback)
```

#### Example Usage

```javascript


    controller.listConsignments(function(error, response, context) {

    
    });
```



### <a name="get_a_single_consignment"></a>![Method: ](https://apidocs.io/img/method.png ".ConsignmentsController.getASingleConsignment") getASingleConsignment

> Returns a single consignment with the requested `id`.


```javascript
function getASingleConsignment(consignmentId, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| consignmentId |  ``` Required ```  | Valid consignment `id`. |



#### Example Usage

```javascript

    var consignmentId = uniqid();

    controller.getASingleConsignment(consignmentId, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="inventory_controller"></a>![Class: ](https://apidocs.io/img/class.png ".InventoryController") InventoryController

### Get singleton instance

The singleton instance of the ``` InventoryController ``` class can be accessed from the API Client.

```javascript
var controller = lib.InventoryController;
```

### <a name="list_inventory_records"></a>![Method: ](https://apidocs.io/img/method.png ".InventoryController.listInventoryRecords") listInventoryRecords

> Returns a paginated list of Inventory records.


```javascript
function listInventoryRecords(callback)
```

#### Example Usage

```javascript


    controller.listInventoryRecords(function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="outlets_controller"></a>![Class: ](https://apidocs.io/img/class.png ".OutletsController") OutletsController

### Get singleton instance

The singleton instance of the ``` OutletsController ``` class can be accessed from the API Client.

```javascript
var controller = lib.OutletsController;
```

### <a name="list_outlets"></a>![Method: ](https://apidocs.io/img/method.png ".OutletsController.listOutlets") listOutlets

> Returns a collection of outlets.


```javascript
function listOutlets(callback)
```

#### Example Usage

```javascript


    controller.listOutlets(function(error, response, context) {

    
    });
```



### <a name="get_a_single_outlet"></a>![Method: ](https://apidocs.io/img/method.png ".OutletsController.getASingleOutlet") getASingleOutlet

> Returns a single outlet with the requested `id`.


```javascript
function getASingleOutlet(outletId, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| outletId |  ``` Required ```  | Valid Outlet `id`. |



#### Example Usage

```javascript

    var outletId = uniqid();

    controller.getASingleOutlet(outletId, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="price_books_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PriceBooksController") PriceBooksController

### Get singleton instance

The singleton instance of the ``` PriceBooksController ``` class can be accessed from the API Client.

```javascript
var controller = lib.PriceBooksController;
```

### <a name="list_price_books"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBooksController.listPriceBooks") listPriceBooks

> Returns a paginated list of price books


```javascript
function listPriceBooks(callback)
```

#### Example Usage

```javascript


    controller.listPriceBooks(function(error, response, context) {

    
    });
```



### <a name="create_a_price_book"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBooksController.createAPriceBook") createAPriceBook

> Creates a new price book.


```javascript
function createAPriceBook(body, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new PriceBookBase({  "name": "Test",  "valid_from": "2018-01-01",  "valid_to": "2019-01-01",  "restrict_to_platform_key": "1",  "customer_group_id": "b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4",  "outlet_id": ""});

    controller.createAPriceBook(body, function(error, response, context) {

    
    });
```



### <a name="get_a_single_price_book"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBooksController.getASinglePriceBook") getASinglePriceBook

> Returns a single price book with a requested `id`


```javascript
function getASinglePriceBook(priceBookId, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| priceBookId |  ``` Required ```  | Valid price book `id`. |



#### Example Usage

```javascript

    var priceBookId = uniqid();

    controller.getASinglePriceBook(priceBookId, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="price_book_products_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PriceBookProductsController") PriceBookProductsController

### Get singleton instance

The singleton instance of the ``` PriceBookProductsController ``` class can be accessed from the API Client.

```javascript
var controller = lib.PriceBookProductsController;
```

### <a name="list_price_book_products"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBookProductsController.listPriceBookProducts") listPriceBookProducts

> Returns a paginated list of price book products.


```javascript
function listPriceBookProducts(callback)
```

#### Example Usage

```javascript


    controller.listPriceBookProducts(function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="products_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductsController") ProductsController

### Get singleton instance

The singleton instance of the ``` ProductsController ``` class can be accessed from the API Client.

```javascript
var controller = lib.ProductsController;
```

### <a name="list_products"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.listProducts") listProducts

> Returns a paginated list of products.


```javascript
function listProducts(callback)
```

#### Example Usage

```javascript


    controller.listProducts(function(error, response, context) {

    
    });
```



### <a name="get_a_single_product"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.getASingleProduct") getASingleProduct

> Returns a single product object with a given `id`.


```javascript
function getASingleProduct(productId, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productId |  ``` Required ```  | Valid product `id`. |



#### Example Usage

```javascript

    var productId = uniqid();

    controller.getASingleProduct(productId, function(error, response, context) {

    
    });
```



### <a name="get_inventory_data_for_a_single_product"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.getInventoryDataForASingleProduct") getInventoryDataForASingleProduct

> Returns inventory data for a single product in all the outlets.


```javascript
function getInventoryDataForASingleProduct(productId, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productId |  ``` Required ```  | Valid product `id`. |



#### Example Usage

```javascript

    var productId = uniqid();

    controller.getInventoryDataForASingleProduct(productId, function(error, response, context) {

    
    });
```



### <a name="upload_an_image"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.uploadAnImage") uploadAnImage

> Upload a binary file with an image to be used for a product.


```javascript
function uploadAnImage(body, productId, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| productId |  ``` Optional ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new UploadAnImageRequest({"key":"value"});
    var productId = product_id;

    controller.uploadAnImage(body, productId, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="product_images_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductImagesController") ProductImagesController

### Get singleton instance

The singleton instance of the ``` ProductImagesController ``` class can be accessed from the API Client.

```javascript
var controller = lib.ProductImagesController;
```

### <a name="get_a_single_product_image_data"></a>![Method: ](https://apidocs.io/img/method.png ".ProductImagesController.getASingleProductImageData") getASingleProductImageData

> Returns the metadata for a single product image with a given `id`.
> This method is useful for checking the status of an image after it was uploaded.


```javascript
function getASingleProductImageData(productImageId, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productImageId |  ``` Required ```  | Valid product `id`. |



#### Example Usage

```javascript

    var productImageId = uniqid();

    controller.getASingleProductImageData(productImageId, function(error, response, context) {

    
    });
```



### <a name="update_set_image_position"></a>![Method: ](https://apidocs.io/img/method.png ".ProductImagesController.updateSetImagePosition") updateSetImagePosition

> Allows for changing the image position in the list


```javascript
function updateSetImagePosition(body, productImageId, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| productImageId |  ``` Optional ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var body = new ImagePosition({  "position": 1});
    var productImageId = product_image_id;

    controller.updateSetImagePosition(body, productImageId, function(error, response, context) {

    
    });
```



### <a name="delete_a_product_image"></a>![Method: ](https://apidocs.io/img/method.png ".ProductImagesController.deleteAProductImage") deleteAProductImage

> Deletes the product_image with the requested `id`.


```javascript
function deleteAProductImage(productImageId, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productImageId |  ``` Optional ```  | TODO: Add a parameter description |



#### Example Usage

```javascript

    var productImageId = product_image_id;

    controller.deleteAProductImage(productImageId, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="product_types_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductTypesController") ProductTypesController

### Get singleton instance

The singleton instance of the ``` ProductTypesController ``` class can be accessed from the API Client.

```javascript
var controller = lib.ProductTypesController;
```

### <a name="list_product_types"></a>![Method: ](https://apidocs.io/img/method.png ".ProductTypesController.listProductTypes") listProductTypes

> Returns a paginated list of product types.


```javascript
function listProductTypes(callback)
```

#### Example Usage

```javascript


    controller.listProductTypes(function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="registers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".RegistersController") RegistersController

### Get singleton instance

The singleton instance of the ``` RegistersController ``` class can be accessed from the API Client.

```javascript
var controller = lib.RegistersController;
```

### <a name="list_registers"></a>![Method: ](https://apidocs.io/img/method.png ".RegistersController.listRegisters") listRegisters

> Returns a paginated list of registers.


```javascript
function listRegisters(callback)
```

#### Example Usage

```javascript


    controller.listRegisters(function(error, response, context) {

    
    });
```



### <a name="get_a_single_register"></a>![Method: ](https://apidocs.io/img/method.png ".RegistersController.getASingleRegister") getASingleRegister

> Returns a single register with the requested `id`.


```javascript
function getASingleRegister(registerId, callback)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| registerId |  ``` Required ```  | Valid register `id`. |



#### Example Usage

```javascript

    var registerId = uniqid();

    controller.getASingleRegister(registerId, function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="tags_controller"></a>![Class: ](https://apidocs.io/img/class.png ".TagsController") TagsController

### Get singleton instance

The singleton instance of the ``` TagsController ``` class can be accessed from the API Client.

```javascript
var controller = lib.TagsController;
```

### <a name="list_tags"></a>![Method: ](https://apidocs.io/img/method.png ".TagsController.listTags") listTags

> Returns a collection of tags.


```javascript
function listTags(callback)
```

#### Example Usage

```javascript


    controller.listTags(function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="sales_controller"></a>![Class: ](https://apidocs.io/img/class.png ".SalesController") SalesController

### Get singleton instance

The singleton instance of the ``` SalesController ``` class can be accessed from the API Client.

```javascript
var controller = lib.SalesController;
```

### <a name="list_sales"></a>![Method: ](https://apidocs.io/img/method.png ".SalesController.listSales") listSales

> Returns a paginated list of Sales.


```javascript
function listSales(callback)
```

#### Example Usage

```javascript


    controller.listSales(function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)

## <a name="suppliers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".SuppliersController") SuppliersController

### Get singleton instance

The singleton instance of the ``` SuppliersController ``` class can be accessed from the API Client.

```javascript
var controller = lib.SuppliersController;
```

### <a name="list_suppliers"></a>![Method: ](https://apidocs.io/img/method.png ".SuppliersController.listSuppliers") listSuppliers

> Returns a paginated list of suppliers.


```javascript
function listSuppliers(callback)
```

#### Example Usage

```javascript


    controller.listSuppliers(function(error, response, context) {

    
    });
```



[Back to List of Controllers](#list_of_controllers)



