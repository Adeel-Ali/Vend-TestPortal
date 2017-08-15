# Getting started

TODO: Add a description

## How to Build

The generated code uses a few Gradle dependencies e.g., Jackson, Volley,
and Apache HttpClient. The reference to these dependencies is already
added in the build.gradle file will be installed automatically. Therefore,
you will need internet access for a successful build.

* In order to open the client library in Android Studio click on ``` Open an Existing Android Project ```.

![Importing SDK into Android Studio - Step 1](https://apidocs.io/illustration/android?step=import1&workspaceFolder=Vend%20REST%20API%202.0&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20Lib&rootNamespace=com.example.www)

* Browse to locate the folder containing the source code. Select the location of the VendRESTAPI20 gradle project and click ``` Ok ```.

![Importing SDK into Android Studio - Step 2](https://apidocs.io/illustration/android?step=import2&workspaceFolder=Vend%20REST%20API%202.0&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20Lib&rootNamespace=com.example.www)

* Upon successful import, the project can be built by clicking on ``` Build > Make Project ``` or  pressing ``` Ctrl + F9 ```.

![Importing SDK into Android Studio - Step 3](https://apidocs.io/illustration/android?step=import3&workspaceFolder=Vend%20REST%20API%202.0&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20Lib&rootNamespace=com.example.www)

## How to Use

The following section explains how to use the VendRESTAPI20 library in a new project.

### 1. Starting a new project 

For starting a new project, click on ``` Create New Android Studio Project ```.

![Add a new project in Android Studio - Step 1](https://apidocs.io/illustration/android?step=createNewProject0&workspaceFolder=Vend%20REST%20API%202.0&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20Lib&rootNamespace=com.example.www)

Here, configure the new project by adding the name, domain and location of the sample application followed by clicking ``` Next ```.

![Create a new Android Studio Project - Step 2](https://apidocs.io/illustration/android?step=createNewProject1&workspaceFolder=Vend%20REST%20API%202.0&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20Lib&rootNamespace=com.example.www)

Following this, select the ``` Phone and Tablet ```` option as shown in the illustration below and click ``` Next ```. 

![Create a new Android Studio Project - Step 3](https://apidocs.io/illustration/android?step=createNewProject2&workspaceFolder=Vend%20REST%20API%202.0&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20Lib&rootNamespace=com.example.www)

In the following step, choose ``` Empty Activity ``` as the activity type and click ``` Next ```.

![Create a new Android Studio Project - Step 4](https://apidocs.io/illustration/android?step=createNewProject3&workspaceFolder=Vend%20REST%20API%202.0&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20Lib&rootNamespace=com.example.www)

In this step, provide an ``` Activity Name ``` and ``` Layout Name ``` and click ``` Finish ```.  This would take you to the newly created project.

![Create a new Android Studio Project - Step 4](https://apidocs.io/illustration/android?step=createNewProject4&workspaceFolder=Vend%20REST%20API%202.0&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20Lib&rootNamespace=com.example.www)

### 2. Add reference of the library project

In order to add a dependency to this sample application, click on the android button shown in the project explorer on the left side as shown in the picture. Click on ``` Project ``` in the drop down that emerges.  

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/android?step=testProject0&workspaceFolder=Vend%20REST%20API%202.0&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20Lib&rootNamespace=com.example.www)

Right click the sample application in the project explorer and click on ``` New > Module ```  as shown in the picture.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/android?step=testProject1&workspaceFolder=Vend%20REST%20API%202.0&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20Lib&rootNamespace=com.example.www)

Choose ``` Import Gradle Project ``` and click ``` Next ```.

![Adding dependency to the client library - Step 3](https://apidocs.io/illustration/android?step=testProject2&workspaceFolder=Vend%20REST%20API%202.0&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20Lib&rootNamespace=com.example.www)

Click on ``` Finish ``` which would take you back to the sample application with the refernced SDK. 

![Adding dependency to the client library - Step 4](https://apidocs.io/illustration/android?step=testProject3&workspaceFolder=Vend%20REST%20API%202.0&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20Lib&rootNamespace=com.example.www)

In the following step naigate to the ``` SampleApplication >  app > build.gradle ``` file and add the following line ```compile project(path: ':VendRESTAPI20')``` to the dependencies section as shown in the illustration below.

![Adding dependency to the client library - Step 5](https://apidocs.io/illustration/android?step=testProject4&workspaceFolder=Vend%20REST%20API%202.0&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20Lib&rootNamespace=com.example.www)

Finally, press ``` Sync Now ``` in the warning visible as shown in the picture below.

![Adding dependency to the client library - Step 6](https://apidocs.io/illustration/android?step=testProject5&workspaceFolder=Vend%20REST%20API%202.0&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20Lib&rootNamespace=com.example.www)

### 3. Write sample code

Once the ``` SampleApplication ``` is created, a file named ``` SampleApplication > app > src > main > java > MainActivity ``` will be visible in the *Project Explorer* with an ``` onCreate ``` method. This is the entry point for the execution of the created project.
Here, you can add code to initialize the client library and instantiate a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

## How to Test

The generated code and the server can be tested using automatically generated test cases. 
JUnit is used as the testing framework and test runner.

In Android Studio, for running the tests do the following:

1. Right click on *SampleApplication > VendRESTAPI20Lib > androidTest > java)* from the project explorer.
2. Select "Run All Tests" or use "Ctrl + Shift + F10" to run the Tests.

## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| oAuthAccessToken | OAuth 2.0 Access Token |



API client can be initialized as following. The `appContext` being passed is the Android application [`Context`](https://developer.android.com/reference/android/content/Context.html).

```java
// Configuration parameters and credentials
String oAuthAccessToken = "oAuthAccessToken"; // OAuth 2.0 Access Token

com.example.www.Configuration.initialize(appContext);
VendRESTAPI20Client client = new VendRESTAPI20Client(oAuthAccessToken);
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

## <a name="brands_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.www.controllers.BrandsController") BrandsController

### Get singleton instance

The singleton instance of the ``` BrandsController ``` class can be accessed from the API Client.

```java
BrandsController brands = client.getBrands();
```

### <a name="list_brands_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.BrandsController.listBrandsAsync") listBrandsAsync

> Returns a paginated list of brands.


```java
void listBrandsAsync(final APICallBack<BrandCollection> callBack)
```

#### Example Usage

```java
// Invoking the API call with sample inputs
brands.listBrandsAsync(new APICallBack<BrandCollection>() {
    public void onSuccess(HttpContext context, BrandCollection response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="customers_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.www.controllers.CustomersController") CustomersController

### Get singleton instance

The singleton instance of the ``` CustomersController ``` class can be accessed from the API Client.

```java
CustomersController customers = client.getCustomers();
```

### <a name="list_customers_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.CustomersController.listCustomersAsync") listCustomersAsync

> Returns a paginated list of customers.


```java
void listCustomersAsync(final APICallBack<CustomerCollection> callBack)
```

#### Example Usage

```java
// Invoking the API call with sample inputs
customers.listCustomersAsync(new APICallBack<CustomerCollection>() {
    public void onSuccess(HttpContext context, CustomerCollection response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="create_a_new_customer_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.CustomersController.createANewCustomerAsync") createANewCustomerAsync

> Creates a new customer.


```java
void createANewCustomerAsync(
        final CustomerBase body,
        final APICallBack<CustomerResponse> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    String bodyValue = "{  \"customer_code\": \"Tony-QKG3\",  \"customer_group_id\": \"b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4\",  \"enable_loyalty\": true,  \"first_name\": \"Tony\",  \"last_name\": \"Stark\",  \"email\": \"ironman@avengers.com\",  \"note\": \"\",  \"gender\": \"M\",  \"date_of_birth\": \"1963-03-03\",  \"company_name\": \"Stark Inc.\",  \"phone\": \"\",  \"mobile\": \"\",  \"fax\": \"\",  \"twitter\": \"\",  \"website\": \"\",  \"physical_address_1\": \"\",  \"physical_address_2\": \"\",  \"physical_suburb\": \"\",  \"physical_city\": \"\",  \"physical_postcode\": \"\",  \"physical_state\": \"\",  \"physical_country_id\": \"US\",  \"postal_address_1\": \"\",  \"postal_address_2\": \"\",  \"postal_suburb\": \"\",  \"postal_city\": \"\",  \"postal_postcode\": \"\",  \"postal_state\": \"\",  \"postal_country_id\": \"\",  \"custom_field_1\": \"\",  \"custom_field_2\": \"\",  \"custom_field_3\": \"\",  \"custom_field_4\": \"\"}";
    CustomerBase body = mapper.readValue(bodyValue,new TypeReference<CustomerBase> (){});
    // Invoking the API call with sample inputs
    customers.createANewCustomerAsync(body, new APICallBack<CustomerResponse>() {
        public void onSuccess(HttpContext context, CustomerResponse response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    });
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


### <a name="get_a_single_customer_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.CustomersController.getASingleCustomerAsync") getASingleCustomerAsync

> Returns a single customer with a requested `id`.


```java
void getASingleCustomerAsync(
        final UUID customerId,
        final APICallBack<CustomerResponse> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |


#### Example Usage

```java
UUID customerId = UUID.randomUUID();
// Invoking the API call with sample inputs
customers.getASingleCustomerAsync(customerId, new APICallBack<CustomerResponse>() {
    public void onSuccess(HttpContext context, CustomerResponse response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="update_a_customer_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.CustomersController.updateACustomerAsync") updateACustomerAsync

> Updates editable fields for the customer with the requested `id`.


```java
void updateACustomerAsync(
        final UUID customerId,
        final CustomerBase body,
        final APICallBack<CustomerResponse> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    UUID customerId = UUID.randomUUID();
    CustomerBase body = new CustomerBase();
    // Invoking the API call with sample inputs
    customers.updateACustomerAsync(customerId, body, new APICallBack<CustomerResponse>() {
        public void onSuccess(HttpContext context, CustomerResponse response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    });
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


### <a name="delete_a_customer_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.CustomersController.deleteACustomerAsync") deleteACustomerAsync

> Deletes the customer with the requested `id`.


```java
void deleteACustomerAsync(
        final UUID customerId,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |


#### Example Usage

```java
UUID customerId = UUID.randomUUID();
// Invoking the API call with sample inputs
customers.deleteACustomerAsync(customerId, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="customer_groups_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.www.controllers.CustomerGroupsController") CustomerGroupsController

### Get singleton instance

The singleton instance of the ``` CustomerGroupsController ``` class can be accessed from the API Client.

```java
CustomerGroupsController customerGroups = client.getCustomerGroups();
```

### <a name="list_customer_groups_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.CustomerGroupsController.listCustomerGroupsAsync") listCustomerGroupsAsync

> Returns a paginated list of customer groups.


```java
void listCustomerGroupsAsync(final APICallBack<CustomerGroupCollection> callBack)
```

#### Example Usage

```java
// Invoking the API call with sample inputs
customerGroups.listCustomerGroupsAsync(new APICallBack<CustomerGroupCollection>() {
    public void onSuccess(HttpContext context, CustomerGroupCollection response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="consignments_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.www.controllers.ConsignmentsController") ConsignmentsController

### Get singleton instance

The singleton instance of the ``` ConsignmentsController ``` class can be accessed from the API Client.

```java
ConsignmentsController consignments = client.getConsignments();
```

### <a name="list_consignments_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.ConsignmentsController.listConsignmentsAsync") listConsignmentsAsync

> Returns a paginated list of consignments.


```java
void listConsignmentsAsync(final APICallBack<ConsignmentCollection> callBack)
```

#### Example Usage

```java
// Invoking the API call with sample inputs
consignments.listConsignmentsAsync(new APICallBack<ConsignmentCollection>() {
    public void onSuccess(HttpContext context, ConsignmentCollection response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="get_a_single_consignment_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.ConsignmentsController.getASingleConsignmentAsync") getASingleConsignmentAsync

> Returns a single consignment with the requested `id`.


```java
void getASingleConsignmentAsync(
        final UUID consignmentId,
        final APICallBack<ConsignmentResponse> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| consignmentId |  ``` Required ```  | Valid consignment `id`. |


#### Example Usage

```java
UUID consignmentId = UUID.randomUUID();
// Invoking the API call with sample inputs
consignments.getASingleConsignmentAsync(consignmentId, new APICallBack<ConsignmentResponse>() {
    public void onSuccess(HttpContext context, ConsignmentResponse response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="inventory_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.www.controllers.InventoryController") InventoryController

### Get singleton instance

The singleton instance of the ``` InventoryController ``` class can be accessed from the API Client.

```java
InventoryController inventory = client.getInventory();
```

### <a name="list_inventory_records_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.InventoryController.listInventoryRecordsAsync") listInventoryRecordsAsync

> Returns a paginated list of Inventory records.


```java
void listInventoryRecordsAsync(final APICallBack<InventoryCollection> callBack)
```

#### Example Usage

```java
// Invoking the API call with sample inputs
inventory.listInventoryRecordsAsync(new APICallBack<InventoryCollection>() {
    public void onSuccess(HttpContext context, InventoryCollection response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="outlets_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.www.controllers.OutletsController") OutletsController

### Get singleton instance

The singleton instance of the ``` OutletsController ``` class can be accessed from the API Client.

```java
OutletsController outlets = client.getOutlets();
```

### <a name="list_outlets_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.OutletsController.listOutletsAsync") listOutletsAsync

> Returns a collection of outlets.


```java
void listOutletsAsync(final APICallBack<OutletCollection> callBack)
```

#### Example Usage

```java
// Invoking the API call with sample inputs
outlets.listOutletsAsync(new APICallBack<OutletCollection>() {
    public void onSuccess(HttpContext context, OutletCollection response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="get_a_single_outlet_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.OutletsController.getASingleOutletAsync") getASingleOutletAsync

> Returns a single outlet with the requested `id`.


```java
void getASingleOutletAsync(
        final UUID outletId,
        final APICallBack<OutletCollection> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| outletId |  ``` Required ```  | Valid Outlet `id`. |


#### Example Usage

```java
UUID outletId = UUID.randomUUID();
// Invoking the API call with sample inputs
outlets.getASingleOutletAsync(outletId, new APICallBack<OutletCollection>() {
    public void onSuccess(HttpContext context, OutletCollection response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="price_books_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.www.controllers.PriceBooksController") PriceBooksController

### Get singleton instance

The singleton instance of the ``` PriceBooksController ``` class can be accessed from the API Client.

```java
PriceBooksController priceBooks = client.getPriceBooks();
```

### <a name="list_price_books_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.PriceBooksController.listPriceBooksAsync") listPriceBooksAsync

> Returns a paginated list of price books


```java
void listPriceBooksAsync(final APICallBack<PriceBookCollection> callBack)
```

#### Example Usage

```java
// Invoking the API call with sample inputs
priceBooks.listPriceBooksAsync(new APICallBack<PriceBookCollection>() {
    public void onSuccess(HttpContext context, PriceBookCollection response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="create_a_price_book_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.PriceBooksController.createAPriceBookAsync") createAPriceBookAsync

> Creates a new price book.


```java
void createAPriceBookAsync(
        final PriceBookBase body,
        final APICallBack<PriceBookResponse> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    String bodyValue = "{  \"name\": \"Test\",  \"valid_from\": \"2018-01-01\",  \"valid_to\": \"2019-01-01\",  \"restrict_to_platform_key\": \"1\",  \"customer_group_id\": \"b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4\",  \"outlet_id\": \"\"}";
    PriceBookBase body = mapper.readValue(bodyValue,new TypeReference<PriceBookBase> (){});
    // Invoking the API call with sample inputs
    priceBooks.createAPriceBookAsync(body, new APICallBack<PriceBookResponse>() {
        public void onSuccess(HttpContext context, PriceBookResponse response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    });
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


### <a name="get_a_single_price_book_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.PriceBooksController.getASinglePriceBookAsync") getASinglePriceBookAsync

> Returns a single price book with a requested `id`


```java
void getASinglePriceBookAsync(
        final UUID priceBookId,
        final APICallBack<PriceBookResponse> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| priceBookId |  ``` Required ```  | Valid price book `id`. |


#### Example Usage

```java
UUID priceBookId = UUID.randomUUID();
// Invoking the API call with sample inputs
priceBooks.getASinglePriceBookAsync(priceBookId, new APICallBack<PriceBookResponse>() {
    public void onSuccess(HttpContext context, PriceBookResponse response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="price_book_products_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.www.controllers.PriceBookProductsController") PriceBookProductsController

### Get singleton instance

The singleton instance of the ``` PriceBookProductsController ``` class can be accessed from the API Client.

```java
PriceBookProductsController priceBookProducts = client.getPriceBookProducts();
```

### <a name="list_price_book_products_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.PriceBookProductsController.listPriceBookProductsAsync") listPriceBookProductsAsync

> Returns a paginated list of price book products.


```java
void listPriceBookProductsAsync(final APICallBack<PriceBookProductCollection> callBack)
```

#### Example Usage

```java
// Invoking the API call with sample inputs
priceBookProducts.listPriceBookProductsAsync(new APICallBack<PriceBookProductCollection>() {
    public void onSuccess(HttpContext context, PriceBookProductCollection response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="products_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.www.controllers.ProductsController") ProductsController

### Get singleton instance

The singleton instance of the ``` ProductsController ``` class can be accessed from the API Client.

```java
ProductsController products = client.getProducts();
```

### <a name="list_products_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.ProductsController.listProductsAsync") listProductsAsync

> Returns a paginated list of products.


```java
void listProductsAsync(final APICallBack<ProductCollection> callBack)
```

#### Example Usage

```java
// Invoking the API call with sample inputs
products.listProductsAsync(new APICallBack<ProductCollection>() {
    public void onSuccess(HttpContext context, ProductCollection response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="get_a_single_product_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.ProductsController.getASingleProductAsync") getASingleProductAsync

> Returns a single product object with a given `id`.


```java
void getASingleProductAsync(
        final UUID productId,
        final APICallBack<ProductResponse> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productId |  ``` Required ```  | Valid product `id`. |


#### Example Usage

```java
UUID productId = UUID.randomUUID();
// Invoking the API call with sample inputs
products.getASingleProductAsync(productId, new APICallBack<ProductResponse>() {
    public void onSuccess(HttpContext context, ProductResponse response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="get_inventory_data_for_a_single_product_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.ProductsController.getInventoryDataForASingleProductAsync") getInventoryDataForASingleProductAsync

> Returns inventory data for a single product in all the outlets.


```java
void getInventoryDataForASingleProductAsync(
        final UUID productId,
        final APICallBack<InventoryCollection> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productId |  ``` Required ```  | Valid product `id`. |


#### Example Usage

```java
UUID productId = UUID.randomUUID();
// Invoking the API call with sample inputs
products.getInventoryDataForASingleProductAsync(productId, new APICallBack<InventoryCollection>() {
    public void onSuccess(HttpContext context, InventoryCollection response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="upload_an_image_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.ProductsController.uploadAnImageAsync") uploadAnImageAsync

> Upload a binary file with an image to be used for a product.


```java
void uploadAnImageAsync(
        final UploadAnImageRequest body,
        final String productId,
        final APICallBack<ImageResponse> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| productId |  ``` Optional ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    UploadAnImageRequest body = new UploadAnImageRequest();
    String productId = "product_id";
    // Invoking the API call with sample inputs
    products.uploadAnImageAsync(body, productId, new APICallBack<ImageResponse>() {
        public void onSuccess(HttpContext context, ImageResponse response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    });
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


[Back to List of Controllers](#list_of_controllers)

## <a name="product_images_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.www.controllers.ProductImagesController") ProductImagesController

### Get singleton instance

The singleton instance of the ``` ProductImagesController ``` class can be accessed from the API Client.

```java
ProductImagesController productImages = client.getProductImages();
```

### <a name="get_a_single_product_image_data_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.ProductImagesController.getASingleProductImageDataAsync") getASingleProductImageDataAsync

> Returns the metadata for a single product image with a given `id`.
> This method is useful for checking the status of an image after it was uploaded.


```java
void getASingleProductImageDataAsync(
        final UUID productImageId,
        final APICallBack<ImageResponse> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productImageId |  ``` Required ```  | Valid product `id`. |


#### Example Usage

```java
UUID productImageId = UUID.randomUUID();
// Invoking the API call with sample inputs
productImages.getASingleProductImageDataAsync(productImageId, new APICallBack<ImageResponse>() {
    public void onSuccess(HttpContext context, ImageResponse response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="update_set_image_position_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.ProductImagesController.updateSetImagePositionAsync") updateSetImagePositionAsync

> Allows for changing the image position in the list


```java
void updateSetImagePositionAsync(
        final ImagePosition body,
        final String productImageId,
        final APICallBack<ImageResponse> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| productImageId |  ``` Optional ```  | TODO: Add a parameter description |


#### Example Usage

```java
try {
    String bodyValue = "{  \"position\": 1}";
    ImagePosition body = mapper.readValue(bodyValue,new TypeReference<ImagePosition> (){});
    String productImageId = "product_image_id";
    // Invoking the API call with sample inputs
    productImages.updateSetImagePositionAsync(body, productImageId, new APICallBack<ImageResponse>() {
        public void onSuccess(HttpContext context, ImageResponse response) {
            // TODO success callback handler
        }
        public void onFailure(HttpContext context, Throwable error) {
            // TODO failure callback handler
        }
    });
} catch(JsonProcessingException e) {
    // TODO Auto-generated catch block
    e.printStackTrace();
}
```


### <a name="delete_a_product_image_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.ProductImagesController.deleteAProductImageAsync") deleteAProductImageAsync

> Deletes the product_image with the requested `id`.


```java
void deleteAProductImageAsync(
        final String productImageId,
        final APICallBack<Object> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productImageId |  ``` Optional ```  | TODO: Add a parameter description |


#### Example Usage

```java
String productImageId = "product_image_id";
// Invoking the API call with sample inputs
productImages.deleteAProductImageAsync(productImageId, new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="product_types_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.www.controllers.ProductTypesController") ProductTypesController

### Get singleton instance

The singleton instance of the ``` ProductTypesController ``` class can be accessed from the API Client.

```java
ProductTypesController productTypes = client.getProductTypes();
```

### <a name="list_product_types_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.ProductTypesController.listProductTypesAsync") listProductTypesAsync

> Returns a paginated list of product types.


```java
void listProductTypesAsync(final APICallBack<ProductTypeCollection> callBack)
```

#### Example Usage

```java
// Invoking the API call with sample inputs
productTypes.listProductTypesAsync(new APICallBack<ProductTypeCollection>() {
    public void onSuccess(HttpContext context, ProductTypeCollection response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="registers_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.www.controllers.RegistersController") RegistersController

### Get singleton instance

The singleton instance of the ``` RegistersController ``` class can be accessed from the API Client.

```java
RegistersController registers = client.getRegisters();
```

### <a name="list_registers_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.RegistersController.listRegistersAsync") listRegistersAsync

> Returns a paginated list of registers.


```java
void listRegistersAsync(final APICallBack<RegisterCollection> callBack)
```

#### Example Usage

```java
// Invoking the API call with sample inputs
registers.listRegistersAsync(new APICallBack<RegisterCollection>() {
    public void onSuccess(HttpContext context, RegisterCollection response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


### <a name="get_a_single_register_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.RegistersController.getASingleRegisterAsync") getASingleRegisterAsync

> Returns a single register with the requested `id`.


```java
void getASingleRegisterAsync(
        final UUID registerId,
        final APICallBack<RegisterCollection> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| registerId |  ``` Required ```  | Valid register `id`. |


#### Example Usage

```java
UUID registerId = UUID.randomUUID();
// Invoking the API call with sample inputs
registers.getASingleRegisterAsync(registerId, new APICallBack<RegisterCollection>() {
    public void onSuccess(HttpContext context, RegisterCollection response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="tags_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.www.controllers.TagsController") TagsController

### Get singleton instance

The singleton instance of the ``` TagsController ``` class can be accessed from the API Client.

```java
TagsController tags = client.getTags();
```

### <a name="list_tags_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.TagsController.listTagsAsync") listTagsAsync

> Returns a collection of tags.


```java
void listTagsAsync(final APICallBack<TagCollection> callBack)
```

#### Example Usage

```java
// Invoking the API call with sample inputs
tags.listTagsAsync(new APICallBack<TagCollection>() {
    public void onSuccess(HttpContext context, TagCollection response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="sales_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.www.controllers.SalesController") SalesController

### Get singleton instance

The singleton instance of the ``` SalesController ``` class can be accessed from the API Client.

```java
SalesController sales = client.getSales();
```

### <a name="list_sales_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.SalesController.listSalesAsync") listSalesAsync

> Returns a paginated list of Sales.


```java
void listSalesAsync(final APICallBack<SaleCollection> callBack)
```

#### Example Usage

```java
// Invoking the API call with sample inputs
sales.listSalesAsync(new APICallBack<SaleCollection>() {
    public void onSuccess(HttpContext context, SaleCollection response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)

## <a name="suppliers_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.example.www.controllers.SuppliersController") SuppliersController

### Get singleton instance

The singleton instance of the ``` SuppliersController ``` class can be accessed from the API Client.

```java
SuppliersController suppliers = client.getSuppliers();
```

### <a name="list_suppliers_async"></a>![Method: ](https://apidocs.io/img/method.png "com.example.www.controllers.SuppliersController.listSuppliersAsync") listSuppliersAsync

> Returns a paginated list of suppliers.


```java
void listSuppliersAsync(final APICallBack<SupplierCollection> callBack)
```

#### Example Usage

```java
// Invoking the API call with sample inputs
suppliers.listSuppliersAsync(new APICallBack<SupplierCollection>() {
    public void onSuccess(HttpContext context, SupplierCollection response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)



