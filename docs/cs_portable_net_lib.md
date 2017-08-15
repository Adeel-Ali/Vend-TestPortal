# Getting started

TODO: Add a description

## How to Build

The generated code uses the Newtonsoft Json.NET NuGet Package. If the automatic NuGet package restore
is enabled, these dependencies will be installed automatically. Therefore,
you will need internet access for build.

1. Open the solution (VendRESTAPI20.sln) file.
2. Invoke the build process using `Ctrl+Shift+B` shortcut key or using the `Build` menu as shown below.

![Building SDK using Visual Studio](https://apidocs.io/illustration/cs?step=buildSDK&workspaceFolder=Vend%20REST%20API%202.0-CSharp&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20.Tests)

## How to Use

The build process generates a portable class library, which can be used like a normal class library. The generated library is compatible with Windows Forms, Windows RT, Windows Phone 8,
Silverlight 5, Xamarin iOS, Xamarin Android and Mono. More information on how to use can be found at the [MSDN Portable Class Libraries documentation](http://msdn.microsoft.com/en-us/library/vstudio/gg597391%28v=vs.100%29.aspx).

The following section explains how to use the VendRESTAPI20 library in a new console project.

### 1. Starting a new project

For starting a new project, right click on the current solution from the *solution explorer* and choose  ``` Add -> New Project ```.

![Add a new project in the existing solution using Visual Studio](https://apidocs.io/illustration/cs?step=addProject&workspaceFolder=Vend%20REST%20API%202.0-CSharp&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20.Tests)

Next, choose "Console Application", provide a ``` TestConsoleProject ``` as the project name and click ``` OK ```.

![Create a new console project using Visual Studio](https://apidocs.io/illustration/cs?step=createProject&workspaceFolder=Vend%20REST%20API%202.0-CSharp&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20.Tests)

### 2. Set as startup project

The new console project is the entry point for the eventual execution. This requires us to set the ``` TestConsoleProject ``` as the start-up project. To do this, right-click on the  ``` TestConsoleProject ``` and choose  ``` Set as StartUp Project ``` form the context menu.

![Set the new cosole project as the start up project](https://apidocs.io/illustration/cs?step=setStartup&workspaceFolder=Vend%20REST%20API%202.0-CSharp&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20.Tests)

### 3. Add reference of the library project

In order to use the VendRESTAPI20 library in the new project, first we must add a projet reference to the ``` TestConsoleProject ```. First, right click on the ``` References ``` node in the *solution explorer* and click ``` Add Reference... ```.

![Open references of the TestConsoleProject](https://apidocs.io/illustration/cs?step=addReference&workspaceFolder=Vend%20REST%20API%202.0-CSharp&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20.Tests)

Next, a window will be displayed where we must set the ``` checkbox ``` on ``` VendRESTAPI20.Tests ``` and click ``` OK ```. By doing this, we have added a reference of the ```VendRESTAPI20.Tests``` project into the new ``` TestConsoleProject ```.

![Add a reference to the TestConsoleProject](https://apidocs.io/illustration/cs?step=createReference&workspaceFolder=Vend%20REST%20API%202.0-CSharp&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20.Tests)

### 4. Write sample code

Once the ``` TestConsoleProject ``` is created, a file named ``` Program.cs ``` will be visible in the *solution explorer* with an empty ``` Main ``` method. This is the entry point for the execution of the entire solution.
Here, you can add code to initialize the client library and acquire the instance of a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

![Add a reference to the TestConsoleProject](https://apidocs.io/illustration/cs?step=addCode&workspaceFolder=Vend%20REST%20API%202.0-CSharp&workspaceName=VendRESTAPI20&projectName=VendRESTAPI20.Tests)

## How to Test

The generated SDK also contain one or more Tests, which are contained in the Tests project.
In order to invoke these test cases, you will need *NUnit 3.0 Test Adapter Extension for Visual Studio*.
Once the SDK is complied, the test cases should appear in the Test Explorer window.
Here, you can click *Run All* to execute these test cases.

## Initialization

### Authentication
In order to setup authentication and initialization of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| oAuthAccessToken | OAuth 2.0 Access Token |



API client can be initialized as following.

```csharp
// Configuration parameters and credentials
string oAuthAccessToken = "oAuthAccessToken"; // OAuth 2.0 Access Token

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

## <a name="brands_controller"></a>![Class: ](https://apidocs.io/img/class.png "VendRESTAPI20.Tests.Controllers.BrandsController") BrandsController

### Get singleton instance

The singleton instance of the ``` BrandsController ``` class can be accessed from the API Client.

```csharp
BrandsController brands = client.Brands;
```

### <a name="list_brands"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.BrandsController.ListBrands") ListBrands

> Returns a paginated list of brands.


```csharp
Task<PCL.Models.BrandCollection> ListBrands()
```

#### Example Usage

```csharp

PCL.Models.BrandCollection result = await brands.ListBrands();

```


[Back to List of Controllers](#list_of_controllers)

## <a name="customers_controller"></a>![Class: ](https://apidocs.io/img/class.png "VendRESTAPI20.Tests.Controllers.CustomersController") CustomersController

### Get singleton instance

The singleton instance of the ``` CustomersController ``` class can be accessed from the API Client.

```csharp
CustomersController customers = client.Customers;
```

### <a name="list_customers"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.CustomersController.ListCustomers") ListCustomers

> Returns a paginated list of customers.


```csharp
Task<PCL.Models.CustomerCollection> ListCustomers()
```

#### Example Usage

```csharp

PCL.Models.CustomerCollection result = await customers.ListCustomers();

```


### <a name="create_a_new_customer"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.CustomersController.CreateANewCustomer") CreateANewCustomer

> Creates a new customer.


```csharp
Task<PCL.Models.CustomerResponse> CreateANewCustomer(PCL.Models.CustomerBase body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string bodyValue = "{  \"customer_code\": \"Tony-QKG3\",  \"customer_group_id\": \"b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4\",  \"enable_loyalty\": true,  \"first_name\": \"Tony\",  \"last_name\": \"Stark\",  \"email\": \"ironman@avengers.com\",  \"note\": \"\",  \"gender\": \"M\",  \"date_of_birth\": \"1963-03-03\",  \"company_name\": \"Stark Inc.\",  \"phone\": \"\",  \"mobile\": \"\",  \"fax\": \"\",  \"twitter\": \"\",  \"website\": \"\",  \"physical_address_1\": \"\",  \"physical_address_2\": \"\",  \"physical_suburb\": \"\",  \"physical_city\": \"\",  \"physical_postcode\": \"\",  \"physical_state\": \"\",  \"physical_country_id\": \"US\",  \"postal_address_1\": \"\",  \"postal_address_2\": \"\",  \"postal_suburb\": \"\",  \"postal_city\": \"\",  \"postal_postcode\": \"\",  \"postal_state\": \"\",  \"postal_country_id\": \"\",  \"custom_field_1\": \"\",  \"custom_field_2\": \"\",  \"custom_field_3\": \"\",  \"custom_field_4\": \"\"}";
var body = Newtonsoft.Json.JsonConvert.DeserializeObject<PCL.Models.CustomerBase>(bodyValue);

PCL.Models.CustomerResponse result = await customers.CreateANewCustomer(body);

```


### <a name="get_a_single_customer"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.CustomersController.GetASingleCustomer") GetASingleCustomer

> Returns a single customer with a requested `id`.


```csharp
Task<PCL.Models.CustomerResponse> GetASingleCustomer(Guid customerId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |


#### Example Usage

```csharp
Guid customerId = Guid.NewGuid();

PCL.Models.CustomerResponse result = await customers.GetASingleCustomer(customerId);

```


### <a name="update_a_customer"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.CustomersController.UpdateACustomer") UpdateACustomer

> Updates editable fields for the customer with the requested `id`.


```csharp
Task<PCL.Models.CustomerResponse> UpdateACustomer(Guid customerId, PCL.Models.CustomerBase body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
Guid customerId = Guid.NewGuid();
var body = new PCL.Models.CustomerBase();

PCL.Models.CustomerResponse result = await customers.UpdateACustomer(customerId, body);

```


### <a name="delete_a_customer"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.CustomersController.DeleteACustomer") DeleteACustomer

> Deletes the customer with the requested `id`.


```csharp
Task DeleteACustomer(Guid customerId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |


#### Example Usage

```csharp
Guid customerId = Guid.NewGuid();

await customers.DeleteACustomer(customerId);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="customer_groups_controller"></a>![Class: ](https://apidocs.io/img/class.png "VendRESTAPI20.Tests.Controllers.CustomerGroupsController") CustomerGroupsController

### Get singleton instance

The singleton instance of the ``` CustomerGroupsController ``` class can be accessed from the API Client.

```csharp
CustomerGroupsController customerGroups = client.CustomerGroups;
```

### <a name="list_customer_groups"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.CustomerGroupsController.ListCustomerGroups") ListCustomerGroups

> Returns a paginated list of customer groups.


```csharp
Task<PCL.Models.CustomerGroupCollection> ListCustomerGroups()
```

#### Example Usage

```csharp

PCL.Models.CustomerGroupCollection result = await customerGroups.ListCustomerGroups();

```


[Back to List of Controllers](#list_of_controllers)

## <a name="consignments_controller"></a>![Class: ](https://apidocs.io/img/class.png "VendRESTAPI20.Tests.Controllers.ConsignmentsController") ConsignmentsController

### Get singleton instance

The singleton instance of the ``` ConsignmentsController ``` class can be accessed from the API Client.

```csharp
ConsignmentsController consignments = client.Consignments;
```

### <a name="list_consignments"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.ConsignmentsController.ListConsignments") ListConsignments

> Returns a paginated list of consignments.


```csharp
Task<PCL.Models.ConsignmentCollection> ListConsignments()
```

#### Example Usage

```csharp

PCL.Models.ConsignmentCollection result = await consignments.ListConsignments();

```


### <a name="get_a_single_consignment"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.ConsignmentsController.GetASingleConsignment") GetASingleConsignment

> Returns a single consignment with the requested `id`.


```csharp
Task<PCL.Models.ConsignmentResponse> GetASingleConsignment(Guid consignmentId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| consignmentId |  ``` Required ```  | Valid consignment `id`. |


#### Example Usage

```csharp
Guid consignmentId = Guid.NewGuid();

PCL.Models.ConsignmentResponse result = await consignments.GetASingleConsignment(consignmentId);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="inventory_controller"></a>![Class: ](https://apidocs.io/img/class.png "VendRESTAPI20.Tests.Controllers.InventoryController") InventoryController

### Get singleton instance

The singleton instance of the ``` InventoryController ``` class can be accessed from the API Client.

```csharp
InventoryController inventory = client.Inventory;
```

### <a name="list_inventory_records"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.InventoryController.ListInventoryRecords") ListInventoryRecords

> Returns a paginated list of Inventory records.


```csharp
Task<PCL.Models.InventoryCollection> ListInventoryRecords()
```

#### Example Usage

```csharp

PCL.Models.InventoryCollection result = await inventory.ListInventoryRecords();

```


[Back to List of Controllers](#list_of_controllers)

## <a name="outlets_controller"></a>![Class: ](https://apidocs.io/img/class.png "VendRESTAPI20.Tests.Controllers.OutletsController") OutletsController

### Get singleton instance

The singleton instance of the ``` OutletsController ``` class can be accessed from the API Client.

```csharp
OutletsController outlets = client.Outlets;
```

### <a name="list_outlets"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.OutletsController.ListOutlets") ListOutlets

> Returns a collection of outlets.


```csharp
Task<PCL.Models.OutletCollection> ListOutlets()
```

#### Example Usage

```csharp

PCL.Models.OutletCollection result = await outlets.ListOutlets();

```


### <a name="get_a_single_outlet"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.OutletsController.GetASingleOutlet") GetASingleOutlet

> Returns a single outlet with the requested `id`.


```csharp
Task<PCL.Models.OutletCollection> GetASingleOutlet(Guid outletId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| outletId |  ``` Required ```  | Valid Outlet `id`. |


#### Example Usage

```csharp
Guid outletId = Guid.NewGuid();

PCL.Models.OutletCollection result = await outlets.GetASingleOutlet(outletId);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="price_books_controller"></a>![Class: ](https://apidocs.io/img/class.png "VendRESTAPI20.Tests.Controllers.PriceBooksController") PriceBooksController

### Get singleton instance

The singleton instance of the ``` PriceBooksController ``` class can be accessed from the API Client.

```csharp
PriceBooksController priceBooks = client.PriceBooks;
```

### <a name="list_price_books"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.PriceBooksController.ListPriceBooks") ListPriceBooks

> Returns a paginated list of price books


```csharp
Task<PCL.Models.PriceBookCollection> ListPriceBooks()
```

#### Example Usage

```csharp

PCL.Models.PriceBookCollection result = await priceBooks.ListPriceBooks();

```


### <a name="create_a_price_book"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.PriceBooksController.CreateAPriceBook") CreateAPriceBook

> Creates a new price book.


```csharp
Task<PCL.Models.PriceBookResponse> CreateAPriceBook(PCL.Models.PriceBookBase body)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string bodyValue = "{  \"name\": \"Test\",  \"valid_from\": \"2018-01-01\",  \"valid_to\": \"2019-01-01\",  \"restrict_to_platform_key\": \"1\",  \"customer_group_id\": \"b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4\",  \"outlet_id\": \"\"}";
var body = Newtonsoft.Json.JsonConvert.DeserializeObject<PCL.Models.PriceBookBase>(bodyValue);

PCL.Models.PriceBookResponse result = await priceBooks.CreateAPriceBook(body);

```


### <a name="get_a_single_price_book"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.PriceBooksController.GetASinglePriceBook") GetASinglePriceBook

> Returns a single price book with a requested `id`


```csharp
Task<PCL.Models.PriceBookResponse> GetASinglePriceBook(Guid priceBookId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| priceBookId |  ``` Required ```  | Valid price book `id`. |


#### Example Usage

```csharp
Guid priceBookId = Guid.NewGuid();

PCL.Models.PriceBookResponse result = await priceBooks.GetASinglePriceBook(priceBookId);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="price_book_products_controller"></a>![Class: ](https://apidocs.io/img/class.png "VendRESTAPI20.Tests.Controllers.PriceBookProductsController") PriceBookProductsController

### Get singleton instance

The singleton instance of the ``` PriceBookProductsController ``` class can be accessed from the API Client.

```csharp
PriceBookProductsController priceBookProducts = client.PriceBookProducts;
```

### <a name="list_price_book_products"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.PriceBookProductsController.ListPriceBookProducts") ListPriceBookProducts

> Returns a paginated list of price book products.


```csharp
Task<PCL.Models.PriceBookProductCollection> ListPriceBookProducts()
```

#### Example Usage

```csharp

PCL.Models.PriceBookProductCollection result = await priceBookProducts.ListPriceBookProducts();

```


[Back to List of Controllers](#list_of_controllers)

## <a name="products_controller"></a>![Class: ](https://apidocs.io/img/class.png "VendRESTAPI20.Tests.Controllers.ProductsController") ProductsController

### Get singleton instance

The singleton instance of the ``` ProductsController ``` class can be accessed from the API Client.

```csharp
ProductsController products = client.Products;
```

### <a name="list_products"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.ProductsController.ListProducts") ListProducts

> Returns a paginated list of products.


```csharp
Task<PCL.Models.ProductCollection> ListProducts()
```

#### Example Usage

```csharp

PCL.Models.ProductCollection result = await products.ListProducts();

```


### <a name="get_a_single_product"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.ProductsController.GetASingleProduct") GetASingleProduct

> Returns a single product object with a given `id`.


```csharp
Task<PCL.Models.ProductResponse> GetASingleProduct(Guid productId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productId |  ``` Required ```  | Valid product `id`. |


#### Example Usage

```csharp
Guid productId = Guid.NewGuid();

PCL.Models.ProductResponse result = await products.GetASingleProduct(productId);

```


### <a name="get_inventory_data_for_a_single_product"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.ProductsController.GetInventoryDataForASingleProduct") GetInventoryDataForASingleProduct

> Returns inventory data for a single product in all the outlets.


```csharp
Task<PCL.Models.InventoryCollection> GetInventoryDataForASingleProduct(Guid productId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productId |  ``` Required ```  | Valid product `id`. |


#### Example Usage

```csharp
Guid productId = Guid.NewGuid();

PCL.Models.InventoryCollection result = await products.GetInventoryDataForASingleProduct(productId);

```


### <a name="upload_an_image"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.ProductsController.UploadAnImage") UploadAnImage

> Upload a binary file with an image to be used for a product.


```csharp
Task<PCL.Models.ImageResponse> UploadAnImage(PCL.Models.UploadAnImageRequest body, string productId = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| productId |  ``` Optional ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
var body = new PCL.Models.UploadAnImageRequest();
string productId = "product_id";

PCL.Models.ImageResponse result = await products.UploadAnImage(body, productId);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="product_images_controller"></a>![Class: ](https://apidocs.io/img/class.png "VendRESTAPI20.Tests.Controllers.ProductImagesController") ProductImagesController

### Get singleton instance

The singleton instance of the ``` ProductImagesController ``` class can be accessed from the API Client.

```csharp
ProductImagesController productImages = client.ProductImages;
```

### <a name="get_a_single_product_image_data"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.ProductImagesController.GetASingleProductImageData") GetASingleProductImageData

> Returns the metadata for a single product image with a given `id`.
> This method is useful for checking the status of an image after it was uploaded.


```csharp
Task<PCL.Models.ImageResponse> GetASingleProductImageData(Guid productImageId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productImageId |  ``` Required ```  | Valid product `id`. |


#### Example Usage

```csharp
Guid productImageId = Guid.NewGuid();

PCL.Models.ImageResponse result = await productImages.GetASingleProductImageData(productImageId);

```


### <a name="update_set_image_position"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.ProductImagesController.UpdateSetImagePosition") UpdateSetImagePosition

> Allows for changing the image position in the list


```csharp
Task<PCL.Models.ImageResponse> UpdateSetImagePosition(PCL.Models.ImagePosition body, string productImageId = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| productImageId |  ``` Optional ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string bodyValue = "{  \"position\": 1}";
var body = Newtonsoft.Json.JsonConvert.DeserializeObject<PCL.Models.ImagePosition>(bodyValue);
string productImageId = "product_image_id";

PCL.Models.ImageResponse result = await productImages.UpdateSetImagePosition(body, productImageId);

```


### <a name="delete_a_product_image"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.ProductImagesController.DeleteAProductImage") DeleteAProductImage

> Deletes the product_image with the requested `id`.


```csharp
Task DeleteAProductImage(string productImageId = null)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productImageId |  ``` Optional ```  | TODO: Add a parameter description |


#### Example Usage

```csharp
string productImageId = "product_image_id";

await productImages.DeleteAProductImage(productImageId);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="product_types_controller"></a>![Class: ](https://apidocs.io/img/class.png "VendRESTAPI20.Tests.Controllers.ProductTypesController") ProductTypesController

### Get singleton instance

The singleton instance of the ``` ProductTypesController ``` class can be accessed from the API Client.

```csharp
ProductTypesController productTypes = client.ProductTypes;
```

### <a name="list_product_types"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.ProductTypesController.ListProductTypes") ListProductTypes

> Returns a paginated list of product types.


```csharp
Task<PCL.Models.ProductTypeCollection> ListProductTypes()
```

#### Example Usage

```csharp

PCL.Models.ProductTypeCollection result = await productTypes.ListProductTypes();

```


[Back to List of Controllers](#list_of_controllers)

## <a name="registers_controller"></a>![Class: ](https://apidocs.io/img/class.png "VendRESTAPI20.Tests.Controllers.RegistersController") RegistersController

### Get singleton instance

The singleton instance of the ``` RegistersController ``` class can be accessed from the API Client.

```csharp
RegistersController registers = client.Registers;
```

### <a name="list_registers"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.RegistersController.ListRegisters") ListRegisters

> Returns a paginated list of registers.


```csharp
Task<PCL.Models.RegisterCollection> ListRegisters()
```

#### Example Usage

```csharp

PCL.Models.RegisterCollection result = await registers.ListRegisters();

```


### <a name="get_a_single_register"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.RegistersController.GetASingleRegister") GetASingleRegister

> Returns a single register with the requested `id`.


```csharp
Task<PCL.Models.RegisterCollection> GetASingleRegister(Guid registerId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| registerId |  ``` Required ```  | Valid register `id`. |


#### Example Usage

```csharp
Guid registerId = Guid.NewGuid();

PCL.Models.RegisterCollection result = await registers.GetASingleRegister(registerId);

```


[Back to List of Controllers](#list_of_controllers)

## <a name="tags_controller"></a>![Class: ](https://apidocs.io/img/class.png "VendRESTAPI20.Tests.Controllers.TagsController") TagsController

### Get singleton instance

The singleton instance of the ``` TagsController ``` class can be accessed from the API Client.

```csharp
TagsController tags = client.Tags;
```

### <a name="list_tags"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.TagsController.ListTags") ListTags

> Returns a collection of tags.


```csharp
Task<PCL.Models.TagCollection> ListTags()
```

#### Example Usage

```csharp

PCL.Models.TagCollection result = await tags.ListTags();

```


[Back to List of Controllers](#list_of_controllers)

## <a name="sales_controller"></a>![Class: ](https://apidocs.io/img/class.png "VendRESTAPI20.Tests.Controllers.SalesController") SalesController

### Get singleton instance

The singleton instance of the ``` SalesController ``` class can be accessed from the API Client.

```csharp
SalesController sales = client.Sales;
```

### <a name="list_sales"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.SalesController.ListSales") ListSales

> Returns a paginated list of Sales.


```csharp
Task<PCL.Models.SaleCollection> ListSales()
```

#### Example Usage

```csharp

PCL.Models.SaleCollection result = await sales.ListSales();

```


[Back to List of Controllers](#list_of_controllers)

## <a name="suppliers_controller"></a>![Class: ](https://apidocs.io/img/class.png "VendRESTAPI20.Tests.Controllers.SuppliersController") SuppliersController

### Get singleton instance

The singleton instance of the ``` SuppliersController ``` class can be accessed from the API Client.

```csharp
SuppliersController suppliers = client.Suppliers;
```

### <a name="list_suppliers"></a>![Method: ](https://apidocs.io/img/method.png "VendRESTAPI20.Tests.Controllers.SuppliersController.ListSuppliers") ListSuppliers

> Returns a paginated list of suppliers.


```csharp
Task<PCL.Models.SupplierCollection> ListSuppliers()
```

#### Example Usage

```csharp

PCL.Models.SupplierCollection result = await suppliers.ListSuppliers();

```


[Back to List of Controllers](#list_of_controllers)



