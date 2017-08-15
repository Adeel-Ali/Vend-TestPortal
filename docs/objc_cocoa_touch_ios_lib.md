# Getting started

TODO: Add a description

## How to Build


The generated code has dependencies over external libraries like UniRest. These dependencies are defined in the ```PodFile``` file that comes with the SDK. 
To resolve these dependencies, we use the Cocoapods package manager.
Visit https://guides.cocoapods.org/using/getting-started.html to setup Cocoapods on your system.
Open command prompt and type ```pod --version```. This should display the current version of Cocoapods installed if the installation was successful.

Using command line, navigate to the directory containing the generated files (including ```PodFile```) for the SDK. 
Run the command ```pod install```. This should install all the required dependencies and create the ```pods``` directory in your project directory.

![Installing dependencies using Cocoapods](https://apidocs.io/illustration/objc?step=AddDependencies&workspaceFolder=Vend%20REST%20API%202.0-ObjC&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20&rootNamespace=VendRESTAPI20)

Open the project workspace using the (VendRESTAPI20.xcworkspace) file. Invoke the build process using `Command(⌘)+B` shortcut key or using the `Build` menu as shown below.

![Building SDK using Xcode](https://apidocs.io/illustration/objc?step=BuildSDK&workspaceFolder=Vend%20REST%20API%202.0-ObjC&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20&rootNamespace=VendRESTAPI20)


## How to Use

The generated code is a Cocoa Touch Static Library which can be used in any iOS project. The support for these generated libraries go all the way back to iOS 6.

The following section explains how to use the VendRESTAPI20 library in a new iOS project.     
### 1. Starting a new project
To start a new project, left-click on the ```Create a new Xcode project```.
![Create Test Project - Step 1](https://apidocs.io/illustration/objc?step=Test1&workspaceFolder=Vend%20REST%20API%202.0-ObjC&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20&rootNamespace=VendRESTAPI20)

Next, choose **Single View Application** and click ```Next```.
![Create Test Project - Step 2](https://apidocs.io/illustration/objc?step=Test2&workspaceFolder=Vend%20REST%20API%202.0-ObjC&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20&rootNamespace=VendRESTAPI20)

Provide **Test-Project** as the product name click ```Next```.
![Create Test Project - Step 3](https://apidocs.io/illustration/objc?step=Test3&workspaceFolder=Vend%20REST%20API%202.0-ObjC&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20&rootNamespace=VendRESTAPI20)

Choose the desired location of your project folder and click ```Create```.
![Create Test Project - Step 4](https://apidocs.io/illustration/objc?step=Test4&workspaceFolder=Vend%20REST%20API%202.0-ObjC&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20&rootNamespace=VendRESTAPI20)

### 2. Adding the static library dependency
To add this dependency open a terminal and navigate to your project folder. Next, input ```pod init``` and press enter.
![Add dependency - Step 1](https://apidocs.io/illustration/objc?step=Add0&workspaceFolder=Vend%20REST%20API%202.0-ObjC&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20&rootNamespace=VendRESTAPI20)

Next, open the newly created ```PodFile``` in your favourite text editor. Add the following line : pod 'VendRESTAPI20', :path => 'Vendor/VendRESTAPI20'
![Add dependency - Step 2](https://apidocs.io/illustration/objc?step=Add1&workspaceFolder=Vend%20REST%20API%202.0-ObjC&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20&rootNamespace=VendRESTAPI20)

Execute `pod install` from terminal to install the dependecy in your project. This would add the dependency to the newly created test project.
![Add dependency - Step 3](https://apidocs.io/illustration/objc?step=Add2&workspaceFolder=Vend%20REST%20API%202.0-ObjC&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20&rootNamespace=VendRESTAPI20)


## How to Test

Unit tests in this SDK can be run using Xcode. 

First build the SDK as shown in the steps above and naivgate to the project directory and open the VendRESTAPI20.xcworkspace file.

Go to the test explorer in Xcode as shown in the picture below and click on `run tests` from the menu. 
![Run tests](https://apidocs.io/illustration/objc?step=RunTests&workspaceFolder=Vend%20REST%20API%202.0-ObjC&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20&rootNamespace=VendRESTAPI20)


## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| oAuthAccessToken | OAuth 2.0 Access Token |



Configuration variables can be set as following.
```Objc
// Configuration parameters and credentials
Configuration_OAuthAccessToken = "Configuration_OAuthAccessToken"; // OAuth 2.0 Access Token

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
```objc
Brands* brands = [[Brands alloc]init] ;
```

### <a name="list_brands_with_completion_block"></a>![Method: ](https://apidocs.io/img/method.png ".BrandsController.listBrandsWithCompletionBlock") listBrandsWithCompletionBlock

> Returns a paginated list of brands.


```objc
function listBrandsWithCompletionBlock:(CompletedGetListBrands) onCompleted()
```



#### Example Usage

```objc

    [self.brands listBrandsWithCompletionBlock:  ^(BOOL success, HttpContext* context, BrandCollection* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="customers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CustomersController") CustomersController

### Get singleton instance
```objc
Customers* customers = [[Customers alloc]init] ;
```

### <a name="list_customers_with_completion_block"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.listCustomersWithCompletionBlock") listCustomersWithCompletionBlock

> Returns a paginated list of customers.


```objc
function listCustomersWithCompletionBlock:(CompletedGetListCustomers) onCompleted()
```



#### Example Usage

```objc

    [self.customers listCustomersWithCompletionBlock:  ^(BOOL success, HttpContext* context, CustomerCollection* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_a_new_customer_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.createANewCustomerAsyncWithBody") createANewCustomerAsyncWithBody

> Creates a new customer.


```objc
function createANewCustomerAsyncWithBody:(CustomerBase*) body
                completionBlock:(CompletedPostCreateANewCustomer) onCompleted(body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    CustomerBase* body = (CustomerBase*) [APIHelper jsonDeserialize: @"{  \"customer_code\": \"Tony-QKG3\",  \"customer_group_id\": \"b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4\",  \"enable_loyalty\": true,  \"first_name\": \"Tony\",  \"last_name\": \"Stark\",  \"email\": \"ironman@avengers.com\",  \"note\": \"\",  \"gender\": \"M\",  \"date_of_birth\": \"1963-03-03\",  \"company_name\": \"Stark Inc.\",  \"phone\": \"\",  \"mobile\": \"\",  \"fax\": \"\",  \"twitter\": \"\",  \"website\": \"\",  \"physical_address_1\": \"\",  \"physical_address_2\": \"\",  \"physical_suburb\": \"\",  \"physical_city\": \"\",  \"physical_postcode\": \"\",  \"physical_state\": \"\",  \"physical_country_id\": \"US\",  \"postal_address_1\": \"\",  \"postal_address_2\": \"\",  \"postal_suburb\": \"\",  \"postal_city\": \"\",  \"postal_postcode\": \"\",  \"postal_state\": \"\",  \"postal_country_id\": \"\",  \"custom_field_1\": \"\",  \"custom_field_2\": \"\",  \"custom_field_3\": \"\",  \"custom_field_4\": \"\"}"
                toClass: CustomerBase.class];

    [self.customers createANewCustomerAsyncWithBody: body  completionBlock:^(BOOL success, HttpContext* context, CustomerResponse* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_a_single_customer_async_with_customer_id"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.getASingleCustomerAsyncWithCustomerId") getASingleCustomerAsyncWithCustomerId

> Returns a single customer with a requested `id`.


```objc
function getASingleCustomerAsyncWithCustomerId:(NSUUID*) customerId
                completionBlock:(CompletedGetASingleCustomer) onCompleted(customerId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |





#### Example Usage

```objc
    // Parameters for the API call
    NSUUID* customerId = 123456789;

    [self.customers getASingleCustomerAsyncWithCustomerId: customerId  completionBlock:^(BOOL success, HttpContext* context, CustomerResponse* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="update_a_customer_async_with_customer_id"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.updateACustomerAsyncWithCustomerId") updateACustomerAsyncWithCustomerId

> Updates editable fields for the customer with the requested `id`.


```objc
function updateACustomerAsyncWithCustomerId:(NSUUID*) customerId
                body:(CustomerBase*) body
                completionBlock:(CompletedPutUpdateACustomer) onCompleted(customerId body : body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |
| body |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSUUID* customerId = 123456789;
    CustomerBase* body = [[CustomerBase alloc]init];

    [self.customers updateACustomerAsyncWithCustomerId: customerId body : body  completionBlock:^(BOOL success, HttpContext* context, CustomerResponse* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="delete_a_customer_async_with_customer_id"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.deleteACustomerAsyncWithCustomerId") deleteACustomerAsyncWithCustomerId

> Deletes the customer with the requested `id`.


```objc
function deleteACustomerAsyncWithCustomerId:(NSUUID*) customerId
                completionBlock:(CompletedDeleteACustomer) onCompleted(customerId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |





#### Example Usage

```objc
    // Parameters for the API call
    NSUUID* customerId = 123456789;

    [self.customers deleteACustomerAsyncWithCustomerId: customerId  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="customer_groups_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CustomerGroupsController") CustomerGroupsController

### Get singleton instance
```objc
CustomerGroups* customerGroups = [[CustomerGroups alloc]init] ;
```

### <a name="list_customer_groups_with_completion_block"></a>![Method: ](https://apidocs.io/img/method.png ".CustomerGroupsController.listCustomerGroupsWithCompletionBlock") listCustomerGroupsWithCompletionBlock

> Returns a paginated list of customer groups.


```objc
function listCustomerGroupsWithCompletionBlock:(CompletedGetListCustomerGroups) onCompleted()
```



#### Example Usage

```objc

    [self.customerGroups listCustomerGroupsWithCompletionBlock:  ^(BOOL success, HttpContext* context, CustomerGroupCollection* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="consignments_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ConsignmentsController") ConsignmentsController

### Get singleton instance
```objc
Consignments* consignments = [[Consignments alloc]init] ;
```

### <a name="list_consignments_with_completion_block"></a>![Method: ](https://apidocs.io/img/method.png ".ConsignmentsController.listConsignmentsWithCompletionBlock") listConsignmentsWithCompletionBlock

> Returns a paginated list of consignments.


```objc
function listConsignmentsWithCompletionBlock:(CompletedGetListConsignments) onCompleted()
```



#### Example Usage

```objc

    [self.consignments listConsignmentsWithCompletionBlock:  ^(BOOL success, HttpContext* context, ConsignmentCollection* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_a_single_consignment_async_with_consignment_id"></a>![Method: ](https://apidocs.io/img/method.png ".ConsignmentsController.getASingleConsignmentAsyncWithConsignmentId") getASingleConsignmentAsyncWithConsignmentId

> Returns a single consignment with the requested `id`.


```objc
function getASingleConsignmentAsyncWithConsignmentId:(NSUUID*) consignmentId
                completionBlock:(CompletedGetASingleConsignment) onCompleted(consignmentId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| consignmentId |  ``` Required ```  | Valid consignment `id`. |





#### Example Usage

```objc
    // Parameters for the API call
    NSUUID* consignmentId = 123456789;

    [self.consignments getASingleConsignmentAsyncWithConsignmentId: consignmentId  completionBlock:^(BOOL success, HttpContext* context, ConsignmentResponse* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="inventory_controller"></a>![Class: ](https://apidocs.io/img/class.png ".InventoryController") InventoryController

### Get singleton instance
```objc
Inventory* inventory = [[Inventory alloc]init] ;
```

### <a name="list_inventory_records_with_completion_block"></a>![Method: ](https://apidocs.io/img/method.png ".InventoryController.listInventoryRecordsWithCompletionBlock") listInventoryRecordsWithCompletionBlock

> Returns a paginated list of Inventory records.


```objc
function listInventoryRecordsWithCompletionBlock:(CompletedGetListInventoryRecords) onCompleted()
```



#### Example Usage

```objc

    [self.inventory listInventoryRecordsWithCompletionBlock:  ^(BOOL success, HttpContext* context, InventoryCollection* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="outlets_controller"></a>![Class: ](https://apidocs.io/img/class.png ".OutletsController") OutletsController

### Get singleton instance
```objc
Outlets* outlets = [[Outlets alloc]init] ;
```

### <a name="list_outlets_with_completion_block"></a>![Method: ](https://apidocs.io/img/method.png ".OutletsController.listOutletsWithCompletionBlock") listOutletsWithCompletionBlock

> Returns a collection of outlets.


```objc
function listOutletsWithCompletionBlock:(CompletedGetListOutlets) onCompleted()
```



#### Example Usage

```objc

    [self.outlets listOutletsWithCompletionBlock:  ^(BOOL success, HttpContext* context, OutletCollection* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_a_single_outlet_async_with_outlet_id"></a>![Method: ](https://apidocs.io/img/method.png ".OutletsController.getASingleOutletAsyncWithOutletId") getASingleOutletAsyncWithOutletId

> Returns a single outlet with the requested `id`.


```objc
function getASingleOutletAsyncWithOutletId:(NSUUID*) outletId
                completionBlock:(CompletedGetASingleOutlet) onCompleted(outletId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| outletId |  ``` Required ```  | Valid Outlet `id`. |





#### Example Usage

```objc
    // Parameters for the API call
    NSUUID* outletId = 123456789;

    [self.outlets getASingleOutletAsyncWithOutletId: outletId  completionBlock:^(BOOL success, HttpContext* context, OutletCollection* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="price_books_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PriceBooksController") PriceBooksController

### Get singleton instance
```objc
PriceBooks* priceBooks = [[PriceBooks alloc]init] ;
```

### <a name="list_price_books_with_completion_block"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBooksController.listPriceBooksWithCompletionBlock") listPriceBooksWithCompletionBlock

> Returns a paginated list of price books


```objc
function listPriceBooksWithCompletionBlock:(CompletedGetListPriceBooks) onCompleted()
```



#### Example Usage

```objc

    [self.priceBooks listPriceBooksWithCompletionBlock:  ^(BOOL success, HttpContext* context, PriceBookCollection* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="create_a_price_book_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBooksController.createAPriceBookAsyncWithBody") createAPriceBookAsyncWithBody

> Creates a new price book.


```objc
function createAPriceBookAsyncWithBody:(PriceBookBase*) body
                completionBlock:(CompletedPostCreateAPriceBook) onCompleted(body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    PriceBookBase* body = (PriceBookBase*) [APIHelper jsonDeserialize: @"{  \"name\": \"Test\",  \"valid_from\": \"2018-01-01\",  \"valid_to\": \"2019-01-01\",  \"restrict_to_platform_key\": \"1\",  \"customer_group_id\": \"b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4\",  \"outlet_id\": \"\"}"
                toClass: PriceBookBase.class];

    [self.priceBooks createAPriceBookAsyncWithBody: body  completionBlock:^(BOOL success, HttpContext* context, PriceBookResponse* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_a_single_price_book_async_with_price_book_id"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBooksController.getASinglePriceBookAsyncWithPriceBookId") getASinglePriceBookAsyncWithPriceBookId

> Returns a single price book with a requested `id`


```objc
function getASinglePriceBookAsyncWithPriceBookId:(NSUUID*) priceBookId
                completionBlock:(CompletedGetASinglePriceBook) onCompleted(priceBookId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| priceBookId |  ``` Required ```  | Valid price book `id`. |





#### Example Usage

```objc
    // Parameters for the API call
    NSUUID* priceBookId = 123456789;

    [self.priceBooks getASinglePriceBookAsyncWithPriceBookId: priceBookId  completionBlock:^(BOOL success, HttpContext* context, PriceBookResponse* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="price_book_products_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PriceBookProductsController") PriceBookProductsController

### Get singleton instance
```objc
PriceBookProducts* priceBookProducts = [[PriceBookProducts alloc]init] ;
```

### <a name="list_price_book_products_with_completion_block"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBookProductsController.listPriceBookProductsWithCompletionBlock") listPriceBookProductsWithCompletionBlock

> Returns a paginated list of price book products.


```objc
function listPriceBookProductsWithCompletionBlock:(CompletedGetListPriceBookProducts) onCompleted()
```



#### Example Usage

```objc

    [self.priceBookProducts listPriceBookProductsWithCompletionBlock:  ^(BOOL success, HttpContext* context, PriceBookProductCollection* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="products_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductsController") ProductsController

### Get singleton instance
```objc
Products* products = [[Products alloc]init] ;
```

### <a name="list_products_with_completion_block"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.listProductsWithCompletionBlock") listProductsWithCompletionBlock

> Returns a paginated list of products.


```objc
function listProductsWithCompletionBlock:(CompletedGetListProducts) onCompleted()
```



#### Example Usage

```objc

    [self.products listProductsWithCompletionBlock:  ^(BOOL success, HttpContext* context, ProductCollection* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_a_single_product_async_with_product_id"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.getASingleProductAsyncWithProductId") getASingleProductAsyncWithProductId

> Returns a single product object with a given `id`.


```objc
function getASingleProductAsyncWithProductId:(NSUUID*) productId
                completionBlock:(CompletedGetASingleProduct) onCompleted(productId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productId |  ``` Required ```  | Valid product `id`. |





#### Example Usage

```objc
    // Parameters for the API call
    NSUUID* productId = 123456789;

    [self.products getASingleProductAsyncWithProductId: productId  completionBlock:^(BOOL success, HttpContext* context, ProductResponse* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_inventory_data_for_a_single_product_async_with_product_id"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.getInventoryDataForASingleProductAsyncWithProductId") getInventoryDataForASingleProductAsyncWithProductId

> Returns inventory data for a single product in all the outlets.


```objc
function getInventoryDataForASingleProductAsyncWithProductId:(NSUUID*) productId
                completionBlock:(CompletedGetInventoryDataForASingleProduct) onCompleted(productId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productId |  ``` Required ```  | Valid product `id`. |





#### Example Usage

```objc
    // Parameters for the API call
    NSUUID* productId = 123456789;

    [self.products getInventoryDataForASingleProductAsyncWithProductId: productId  completionBlock:^(BOOL success, HttpContext* context, InventoryCollection* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="upload_an_image_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.uploadAnImageAsyncWithBody") uploadAnImageAsyncWithBody

> Upload a binary file with an image to be used for a product.


```objc
function uploadAnImageAsyncWithBody:(UploadAnImageRequest*) body
                productId:(NSString*) productId
                completionBlock:(CompletedPostUploadAnImage) onCompleted(body productId : productId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| productId |  ``` Optional ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    UploadAnImageRequest* body = [[UploadAnImageRequest alloc]init];
    NSString* productId = @"product_id";

    [self.products uploadAnImageAsyncWithBody: body productId : productId  completionBlock:^(BOOL success, HttpContext* context, ImageResponse* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="product_images_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductImagesController") ProductImagesController

### Get singleton instance
```objc
ProductImages* productImages = [[ProductImages alloc]init] ;
```

### <a name="get_a_single_product_image_data_async_with_product_image_id"></a>![Method: ](https://apidocs.io/img/method.png ".ProductImagesController.getASingleProductImageDataAsyncWithProductImageId") getASingleProductImageDataAsyncWithProductImageId

> Returns the metadata for a single product image with a given `id`.
> This method is useful for checking the status of an image after it was uploaded.


```objc
function getASingleProductImageDataAsyncWithProductImageId:(NSUUID*) productImageId
                completionBlock:(CompletedGetASingleProductImageData) onCompleted(productImageId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productImageId |  ``` Required ```  | Valid product `id`. |





#### Example Usage

```objc
    // Parameters for the API call
    NSUUID* productImageId = 123456789;

    [self.productImages getASingleProductImageDataAsyncWithProductImageId: productImageId  completionBlock:^(BOOL success, HttpContext* context, ImageResponse* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="update_set_image_position_async_with_body"></a>![Method: ](https://apidocs.io/img/method.png ".ProductImagesController.updateSetImagePositionAsyncWithBody") updateSetImagePositionAsyncWithBody

> Allows for changing the image position in the list


```objc
function updateSetImagePositionAsyncWithBody:(ImagePosition*) body
                productImageId:(NSString*) productImageId
                completionBlock:(CompletedPutSetImagePosition) onCompleted(body productImageId : productImageId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| productImageId |  ``` Optional ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    ImagePosition* body = (ImagePosition*) [APIHelper jsonDeserialize: @"{  \"position\": 1}"
                toClass: ImagePosition.class];
    NSString* productImageId = @"product_image_id";

    [self.productImages updateSetImagePositionAsyncWithBody: body productImageId : productImageId  completionBlock:^(BOOL success, HttpContext* context, ImageResponse* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="delete_a_product_image_async_with_product_image_id"></a>![Method: ](https://apidocs.io/img/method.png ".ProductImagesController.deleteAProductImageAsyncWithProductImageId") deleteAProductImageAsyncWithProductImageId

> Deletes the product_image with the requested `id`.


```objc
function deleteAProductImageAsyncWithProductImageId:(NSString*) productImageId
                completionBlock:(CompletedDeleteAProductImage) onCompleted(productImageId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productImageId |  ``` Optional ```  | TODO: Add a parameter description |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* productImageId = @"product_image_id";

    [self.productImages deleteAProductImageAsyncWithProductImageId: productImageId  completionBlock:^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="product_types_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductTypesController") ProductTypesController

### Get singleton instance
```objc
ProductTypes* productTypes = [[ProductTypes alloc]init] ;
```

### <a name="list_product_types_with_completion_block"></a>![Method: ](https://apidocs.io/img/method.png ".ProductTypesController.listProductTypesWithCompletionBlock") listProductTypesWithCompletionBlock

> Returns a paginated list of product types.


```objc
function listProductTypesWithCompletionBlock:(CompletedGetListProductTypes) onCompleted()
```



#### Example Usage

```objc

    [self.productTypes listProductTypesWithCompletionBlock:  ^(BOOL success, HttpContext* context, ProductTypeCollection* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="registers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".RegistersController") RegistersController

### Get singleton instance
```objc
Registers* registers = [[Registers alloc]init] ;
```

### <a name="list_registers_with_completion_block"></a>![Method: ](https://apidocs.io/img/method.png ".RegistersController.listRegistersWithCompletionBlock") listRegistersWithCompletionBlock

> Returns a paginated list of registers.


```objc
function listRegistersWithCompletionBlock:(CompletedGetListRegisters) onCompleted()
```



#### Example Usage

```objc

    [self.registers listRegistersWithCompletionBlock:  ^(BOOL success, HttpContext* context, RegisterCollection* response, NSError* error) { 
       //Add code here
    }];
```


### <a name="get_a_single_register_async_with_register_id"></a>![Method: ](https://apidocs.io/img/method.png ".RegistersController.getASingleRegisterAsyncWithRegisterId") getASingleRegisterAsyncWithRegisterId

> Returns a single register with the requested `id`.


```objc
function getASingleRegisterAsyncWithRegisterId:(NSUUID*) registerId
                completionBlock:(CompletedGetASingleRegister) onCompleted(registerId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| registerId |  ``` Required ```  | Valid register `id`. |





#### Example Usage

```objc
    // Parameters for the API call
    NSUUID* registerId = 123456789;

    [self.registers getASingleRegisterAsyncWithRegisterId: registerId  completionBlock:^(BOOL success, HttpContext* context, RegisterCollection* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="tags_controller"></a>![Class: ](https://apidocs.io/img/class.png ".TagsController") TagsController

### Get singleton instance
```objc
Tags* tags = [[Tags alloc]init] ;
```

### <a name="list_tags_with_completion_block"></a>![Method: ](https://apidocs.io/img/method.png ".TagsController.listTagsWithCompletionBlock") listTagsWithCompletionBlock

> Returns a collection of tags.


```objc
function listTagsWithCompletionBlock:(CompletedGetListTags) onCompleted()
```



#### Example Usage

```objc

    [self.tags listTagsWithCompletionBlock:  ^(BOOL success, HttpContext* context, TagCollection* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="sales_controller"></a>![Class: ](https://apidocs.io/img/class.png ".SalesController") SalesController

### Get singleton instance
```objc
Sales* sales = [[Sales alloc]init] ;
```

### <a name="list_sales_with_completion_block"></a>![Method: ](https://apidocs.io/img/method.png ".SalesController.listSalesWithCompletionBlock") listSalesWithCompletionBlock

> Returns a paginated list of Sales.


```objc
function listSalesWithCompletionBlock:(CompletedGetListSales) onCompleted()
```



#### Example Usage

```objc

    [self.sales listSalesWithCompletionBlock:  ^(BOOL success, HttpContext* context, SaleCollection* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)

## <a name="suppliers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".SuppliersController") SuppliersController

### Get singleton instance
```objc
Suppliers* suppliers = [[Suppliers alloc]init] ;
```

### <a name="list_suppliers_with_completion_block"></a>![Method: ](https://apidocs.io/img/method.png ".SuppliersController.listSuppliersWithCompletionBlock") listSuppliersWithCompletionBlock

> Returns a paginated list of suppliers.


```objc
function listSuppliersWithCompletionBlock:(CompletedGetListSuppliers) onCompleted()
```



#### Example Usage

```objc

    [self.suppliers listSuppliersWithCompletionBlock:  ^(BOOL success, HttpContext* context, SupplierCollection* response, NSError* error) { 
       //Add code here
    }];
```


[Back to List of Controllers](#list_of_controllers)



