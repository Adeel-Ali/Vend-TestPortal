# Getting started

TODO: Add a description

## How to Build


* In order to successfully build and run your SDK files, you are required to have the following setup in your system:
    * **Go**  (Visit [https://golang.org/doc/install](https://golang.org/doc/install) for more details on how to install Go)
    * **Java VM** Version 8 or later
    * **Eclipse 4.6 (Neon)** or later ([http://www.eclipse.org/neon/](http://www.eclipse.org/neon/))
    * **GoClipse** setup within above installed Eclipse (Follow the instructions at [this link](https://github.com/GoClipse/goclipse/blob/latest/documentation/Installation.md#instructions) to setup GoClipse)
* Ensure that ```GOPATH``` environment variable is set in the system variables. If not, set it to your workspace directory where you will be adding your Go projects.
* The generated code uses unirest-go http library. Therefore, you will need internet access to resolve this dependency. If Go is properly installed and configured, run the following command to pull the dependency:

```Go
go get github.com/apimatic/unirest-go
```

This will install unirest-go in the ```GOPATH``` you specified in the system variables.

Now follow the steps mentioned below to build your SDK:

1. Open eclipse in the Go language perspective and click on the ```Import``` option in ```File``` menu.

![Importing SDK into Eclipse - Step 1](https://apidocs.io/illustration/go?step=import0)

2. Select ```General -> Existing Projects into Workspace``` option from the tree list.

![Importing SDK into Eclipse - Step 2](https://apidocs.io/illustration/go?step=import1)

3. In ```Select root directory```, provide path to the unzipped archive for the generated code. Once the path is set and the Project becomes visible under ```Projects``` click ```Finish```

![Importing SDK into Eclipse - Step 3](https://apidocs.io/illustration/go?step=import2&workspaceFolder=Vend%20REST%20API%202.0-GoLang&projectName=vendrestapi20_lib)

4. The Go library will be imported and its files will be visible in the Project Explorer

![Importing SDK into Eclipse - Step 4](https://apidocs.io/illustration/go?step=import3&projectName=vendrestapi20_lib)

## How to Use

The following section explains how to use the Vendrestapi20Lib library in a new project.

### 1. Add a new Test Project

Create a new project in Eclipse by ```File``` -> ```New``` -> ```Go Project```

![Add a new project in Eclipse](https://apidocs.io/illustration/go?step=createNewProject0)

Name the Project as ```Test``` and click ```Finish```

![Create a new Maven Project - Step 1](https://apidocs.io/illustration/go?step=createNewProject1)

Create a new directory in the ```src``` directory of this project

![Create a new Maven Project - Step 2](https://apidocs.io/illustration/go?step=createNewProject2&projectName=vendrestapi20_lib)

Name it ```test.com```

![Create a new Maven Project - Step 3](https://apidocs.io/illustration/go?step=createNewProject3&projectName=vendrestapi20_lib)

Now create a new file inside ```src/test.com```

![Create a new Maven Project - Step 4](https://apidocs.io/illustration/go?step=createNewProject4&projectName=vendrestapi20_lib)

Name it ```testsdk.go```

![Create a new Maven Project - Step 5](https://apidocs.io/illustration/go?step=createNewProject5&projectName=vendrestapi20_lib)

In this Go file, you can start adding code to initialize the client library. Sample code to initialize the client library and using its methods is given in the subsequent sections.

### 2. Configure the Test Project

You need to import your generated library in this project in order to make use of its functions. In order to import the library, you can add its path in the ```GOPATH``` for this project. Follow the below steps:

Right click on the project name and click on ```Properties```

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/go?step=testProject0&projectName=vendrestapi20_lib)

Choose ```Go Compiler``` from the side menu. Check ```Use project specific settings``` and uncheck ```Use same value as the GOPATH environment variable.```. By default, the GOPATH value from the environment variables will be visible in ```Eclipse GOPATH```. Do not remove this as this points to the unirest dependency.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/go?step=testProject1)

Append the library path to this GOPATH

![Adding dependency to the client library - Step 3](https://apidocs.io/illustration/go?step=testProject2&workspaceFolder=Vend%20REST%20API%202.0-GoLang)

Once the path is appended, click on ```OK```

### 3. Build the Test Project

Right click on the project name and click on ```Build Project```

![Build Project](https://apidocs.io/illustration/go?step=buildProject&projectName=vendrestapi20_lib)

### 4. Run the Test Project

If the build is successful, right click on your Go file and click on ```Run As``` -> ```Go Application```

![Run Project](https://apidocs.io/illustration/go?step=runProject&projectName=vendrestapi20_lib)

## Initialization

### Authentication
In order to setup authentication of the API client, you need the following information.

| Parameter | Description |
|-----------|-------------|
| oAuthAccessToken | OAuth 2.0 Access Token |


To configure these for your generated code, open the file "Configuration.go" and edit it's contents.


# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [brands_pkg](#brands_pkg)
* [customers_pkg](#customers_pkg)
* [customergroups_pkg](#customergroups_pkg)
* [consignments_pkg](#consignments_pkg)
* [inventory_pkg](#inventory_pkg)
* [outlets_pkg](#outlets_pkg)
* [pricebooks_pkg](#pricebooks_pkg)
* [pricebookproducts_pkg](#pricebookproducts_pkg)
* [products_pkg](#products_pkg)
* [productimages_pkg](#productimages_pkg)
* [producttypes_pkg](#producttypes_pkg)
* [registers_pkg](#registers_pkg)
* [tags_pkg](#tags_pkg)
* [sales_pkg](#sales_pkg)
* [suppliers_pkg](#suppliers_pkg)

## <a name="brands_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".brands_pkg") brands_pkg

### Get instance

Factory for the ``` BRANDS ``` interface can be accessed from the package brands_pkg.

```go
brands := brands_pkg.NewBRANDS()
```

### <a name="list_brands"></a>![Method: ](https://apidocs.io/img/method.png ".brands_pkg.ListBrands") ListBrands

> Returns a paginated list of brands.


```go
func (me *BRANDS_IMPL) ListBrands()(*models_pkg.BrandCollection,error)
```

#### Example Usage

```go

var result *models_pkg.BrandCollection
result,_ = brands.ListBrands()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="customers_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".customers_pkg") customers_pkg

### Get instance

Factory for the ``` CUSTOMERS ``` interface can be accessed from the package customers_pkg.

```go
customers := customers_pkg.NewCUSTOMERS()
```

### <a name="list_customers"></a>![Method: ](https://apidocs.io/img/method.png ".customers_pkg.ListCustomers") ListCustomers

> Returns a paginated list of customers.


```go
func (me *CUSTOMERS_IMPL) ListCustomers()(*models_pkg.CustomerCollection,error)
```

#### Example Usage

```go

var result *models_pkg.CustomerCollection
result,_ = customers.ListCustomers()

```


### <a name="create_a_new_customer"></a>![Method: ](https://apidocs.io/img/method.png ".customers_pkg.CreateANewCustomer") CreateANewCustomer

> Creates a new customer.


```go
func (me *CUSTOMERS_IMPL) CreateANewCustomer(body *models_pkg.CustomerBase)(*models_pkg.CustomerResponse,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
bodyValue := []byte("{  \"customer_code\": \"Tony-QKG3\",  \"customer_group_id\": \"b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4\",  \"enable_loyalty\": true,  \"first_name\": \"Tony\",  \"last_name\": \"Stark\",  \"email\": \"ironman@avengers.com\",  \"note\": \"\",  \"gender\": \"M\",  \"date_of_birth\": \"1963-03-03\",  \"company_name\": \"Stark Inc.\",  \"phone\": \"\",  \"mobile\": \"\",  \"fax\": \"\",  \"twitter\": \"\",  \"website\": \"\",  \"physical_address_1\": \"\",  \"physical_address_2\": \"\",  \"physical_suburb\": \"\",  \"physical_city\": \"\",  \"physical_postcode\": \"\",  \"physical_state\": \"\",  \"physical_country_id\": \"US\",  \"postal_address_1\": \"\",  \"postal_address_2\": \"\",  \"postal_suburb\": \"\",  \"postal_city\": \"\",  \"postal_postcode\": \"\",  \"postal_state\": \"\",  \"postal_country_id\": \"\",  \"custom_field_1\": \"\",  \"custom_field_2\": \"\",  \"custom_field_3\": \"\",  \"custom_field_4\": \"\"}")
var body *models_pkg.CustomerBase
json.Unmarshal(bodyValue,&body)

var result *models_pkg.CustomerResponse
result,_ = customers.CreateANewCustomer(body)

```


### <a name="get_a_single_customer"></a>![Method: ](https://apidocs.io/img/method.png ".customers_pkg.GetASingleCustomer") GetASingleCustomer

> Returns a single customer with a requested `id`.


```go
func (me *CUSTOMERS_IMPL) GetASingleCustomer(customerId uuid.UUID)(*models_pkg.CustomerResponse,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |


#### Example Usage

```go
customerId := uuid.NewV4()

var result *models_pkg.CustomerResponse
result,_ = customers.GetASingleCustomer(customerId)

```


### <a name="update_a_customer"></a>![Method: ](https://apidocs.io/img/method.png ".customers_pkg.UpdateACustomer") UpdateACustomer

> Updates editable fields for the customer with the requested `id`.


```go
func (me *CUSTOMERS_IMPL) UpdateACustomer(
            customerId uuid.UUID,
            body *models_pkg.CustomerBase)(*models_pkg.CustomerResponse,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
customerId := uuid.NewV4()
var body *models_pkg.CustomerBase

var result *models_pkg.CustomerResponse
result,_ = customers.UpdateACustomer(customerId, body)

```


### <a name="delete_a_customer"></a>![Method: ](https://apidocs.io/img/method.png ".customers_pkg.DeleteACustomer") DeleteACustomer

> Deletes the customer with the requested `id`.


```go
func (me *CUSTOMERS_IMPL) DeleteACustomer(customerId uuid.UUID)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |


#### Example Usage

```go
customerId := uuid.NewV4()

var result 
result,_ = customers.DeleteACustomer(customerId)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="customergroups_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".customergroups_pkg") customergroups_pkg

### Get instance

Factory for the ``` CUSTOMERGROUPS ``` interface can be accessed from the package customergroups_pkg.

```go
customerGroups := customergroups_pkg.NewCUSTOMERGROUPS()
```

### <a name="list_customer_groups"></a>![Method: ](https://apidocs.io/img/method.png ".customergroups_pkg.ListCustomerGroups") ListCustomerGroups

> Returns a paginated list of customer groups.


```go
func (me *CUSTOMERGROUPS_IMPL) ListCustomerGroups()(*models_pkg.CustomerGroupCollection,error)
```

#### Example Usage

```go

var result *models_pkg.CustomerGroupCollection
result,_ = customerGroups.ListCustomerGroups()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="consignments_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".consignments_pkg") consignments_pkg

### Get instance

Factory for the ``` CONSIGNMENTS ``` interface can be accessed from the package consignments_pkg.

```go
consignments := consignments_pkg.NewCONSIGNMENTS()
```

### <a name="list_consignments"></a>![Method: ](https://apidocs.io/img/method.png ".consignments_pkg.ListConsignments") ListConsignments

> Returns a paginated list of consignments.


```go
func (me *CONSIGNMENTS_IMPL) ListConsignments()(*models_pkg.ConsignmentCollection,error)
```

#### Example Usage

```go

var result *models_pkg.ConsignmentCollection
result,_ = consignments.ListConsignments()

```


### <a name="get_a_single_consignment"></a>![Method: ](https://apidocs.io/img/method.png ".consignments_pkg.GetASingleConsignment") GetASingleConsignment

> Returns a single consignment with the requested `id`.


```go
func (me *CONSIGNMENTS_IMPL) GetASingleConsignment(consignmentId uuid.UUID)(*models_pkg.ConsignmentResponse,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| consignmentId |  ``` Required ```  | Valid consignment `id`. |


#### Example Usage

```go
consignmentId := uuid.NewV4()

var result *models_pkg.ConsignmentResponse
result,_ = consignments.GetASingleConsignment(consignmentId)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="inventory_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".inventory_pkg") inventory_pkg

### Get instance

Factory for the ``` INVENTORY ``` interface can be accessed from the package inventory_pkg.

```go
inventory := inventory_pkg.NewINVENTORY()
```

### <a name="list_inventory_records"></a>![Method: ](https://apidocs.io/img/method.png ".inventory_pkg.ListInventoryRecords") ListInventoryRecords

> Returns a paginated list of Inventory records.


```go
func (me *INVENTORY_IMPL) ListInventoryRecords()(*models_pkg.InventoryCollection,error)
```

#### Example Usage

```go

var result *models_pkg.InventoryCollection
result,_ = inventory.ListInventoryRecords()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="outlets_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".outlets_pkg") outlets_pkg

### Get instance

Factory for the ``` OUTLETS ``` interface can be accessed from the package outlets_pkg.

```go
outlets := outlets_pkg.NewOUTLETS()
```

### <a name="list_outlets"></a>![Method: ](https://apidocs.io/img/method.png ".outlets_pkg.ListOutlets") ListOutlets

> Returns a collection of outlets.


```go
func (me *OUTLETS_IMPL) ListOutlets()(*models_pkg.OutletCollection,error)
```

#### Example Usage

```go

var result *models_pkg.OutletCollection
result,_ = outlets.ListOutlets()

```


### <a name="get_a_single_outlet"></a>![Method: ](https://apidocs.io/img/method.png ".outlets_pkg.GetASingleOutlet") GetASingleOutlet

> Returns a single outlet with the requested `id`.


```go
func (me *OUTLETS_IMPL) GetASingleOutlet(outletId uuid.UUID)(*models_pkg.OutletCollection,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| outletId |  ``` Required ```  | Valid Outlet `id`. |


#### Example Usage

```go
outletId := uuid.NewV4()

var result *models_pkg.OutletCollection
result,_ = outlets.GetASingleOutlet(outletId)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="pricebooks_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".pricebooks_pkg") pricebooks_pkg

### Get instance

Factory for the ``` PRICEBOOKS ``` interface can be accessed from the package pricebooks_pkg.

```go
priceBooks := pricebooks_pkg.NewPRICEBOOKS()
```

### <a name="list_price_books"></a>![Method: ](https://apidocs.io/img/method.png ".pricebooks_pkg.ListPriceBooks") ListPriceBooks

> Returns a paginated list of price books


```go
func (me *PRICEBOOKS_IMPL) ListPriceBooks()(*models_pkg.PriceBookCollection,error)
```

#### Example Usage

```go

var result *models_pkg.PriceBookCollection
result,_ = priceBooks.ListPriceBooks()

```


### <a name="create_a_price_book"></a>![Method: ](https://apidocs.io/img/method.png ".pricebooks_pkg.CreateAPriceBook") CreateAPriceBook

> Creates a new price book.


```go
func (me *PRICEBOOKS_IMPL) CreateAPriceBook(body *models_pkg.PriceBookBase)(*models_pkg.PriceBookResponse,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
bodyValue := []byte("{  \"name\": \"Test\",  \"valid_from\": \"2018-01-01\",  \"valid_to\": \"2019-01-01\",  \"restrict_to_platform_key\": \"1\",  \"customer_group_id\": \"b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4\",  \"outlet_id\": \"\"}")
var body *models_pkg.PriceBookBase
json.Unmarshal(bodyValue,&body)

var result *models_pkg.PriceBookResponse
result,_ = priceBooks.CreateAPriceBook(body)

```


### <a name="get_a_single_price_book"></a>![Method: ](https://apidocs.io/img/method.png ".pricebooks_pkg.GetASinglePriceBook") GetASinglePriceBook

> Returns a single price book with a requested `id`


```go
func (me *PRICEBOOKS_IMPL) GetASinglePriceBook(priceBookId uuid.UUID)(*models_pkg.PriceBookResponse,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| priceBookId |  ``` Required ```  | Valid price book `id`. |


#### Example Usage

```go
priceBookId := uuid.NewV4()

var result *models_pkg.PriceBookResponse
result,_ = priceBooks.GetASinglePriceBook(priceBookId)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="pricebookproducts_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".pricebookproducts_pkg") pricebookproducts_pkg

### Get instance

Factory for the ``` PRICEBOOKPRODUCTS ``` interface can be accessed from the package pricebookproducts_pkg.

```go
priceBookProducts := pricebookproducts_pkg.NewPRICEBOOKPRODUCTS()
```

### <a name="list_price_book_products"></a>![Method: ](https://apidocs.io/img/method.png ".pricebookproducts_pkg.ListPriceBookProducts") ListPriceBookProducts

> Returns a paginated list of price book products.


```go
func (me *PRICEBOOKPRODUCTS_IMPL) ListPriceBookProducts()(*models_pkg.PriceBookProductCollection,error)
```

#### Example Usage

```go

var result *models_pkg.PriceBookProductCollection
result,_ = priceBookProducts.ListPriceBookProducts()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="products_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".products_pkg") products_pkg

### Get instance

Factory for the ``` PRODUCTS ``` interface can be accessed from the package products_pkg.

```go
products := products_pkg.NewPRODUCTS()
```

### <a name="list_products"></a>![Method: ](https://apidocs.io/img/method.png ".products_pkg.ListProducts") ListProducts

> Returns a paginated list of products.


```go
func (me *PRODUCTS_IMPL) ListProducts()(*models_pkg.ProductCollection,error)
```

#### Example Usage

```go

var result *models_pkg.ProductCollection
result,_ = products.ListProducts()

```


### <a name="get_a_single_product"></a>![Method: ](https://apidocs.io/img/method.png ".products_pkg.GetASingleProduct") GetASingleProduct

> Returns a single product object with a given `id`.


```go
func (me *PRODUCTS_IMPL) GetASingleProduct(productId uuid.UUID)(*models_pkg.ProductResponse,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productId |  ``` Required ```  | Valid product `id`. |


#### Example Usage

```go
productId := uuid.NewV4()

var result *models_pkg.ProductResponse
result,_ = products.GetASingleProduct(productId)

```


### <a name="get_inventory_data_for_a_single_product"></a>![Method: ](https://apidocs.io/img/method.png ".products_pkg.GetInventoryDataForASingleProduct") GetInventoryDataForASingleProduct

> Returns inventory data for a single product in all the outlets.


```go
func (me *PRODUCTS_IMPL) GetInventoryDataForASingleProduct(productId uuid.UUID)(*models_pkg.InventoryCollection,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productId |  ``` Required ```  | Valid product `id`. |


#### Example Usage

```go
productId := uuid.NewV4()

var result *models_pkg.InventoryCollection
result,_ = products.GetInventoryDataForASingleProduct(productId)

```


### <a name="upload_an_image"></a>![Method: ](https://apidocs.io/img/method.png ".products_pkg.UploadAnImage") UploadAnImage

> Upload a binary file with an image to be used for a product.


```go
func (me *PRODUCTS_IMPL) UploadAnImage(
            body *models_pkg.UploadAnImageRequest,
            productId *string)(*models_pkg.ImageResponse,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| productId |  ``` Optional ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.UploadAnImageRequest
productId := "product_id"

var result *models_pkg.ImageResponse
result,_ = products.UploadAnImage(body, productId)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="productimages_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".productimages_pkg") productimages_pkg

### Get instance

Factory for the ``` PRODUCTIMAGES ``` interface can be accessed from the package productimages_pkg.

```go
productImages := productimages_pkg.NewPRODUCTIMAGES()
```

### <a name="get_a_single_product_image_data"></a>![Method: ](https://apidocs.io/img/method.png ".productimages_pkg.GetASingleProductImageData") GetASingleProductImageData

> Returns the metadata for a single product image with a given `id`.
> This method is useful for checking the status of an image after it was uploaded.


```go
func (me *PRODUCTIMAGES_IMPL) GetASingleProductImageData(productImageId uuid.UUID)(*models_pkg.ImageResponse,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productImageId |  ``` Required ```  | Valid product `id`. |


#### Example Usage

```go
productImageId := uuid.NewV4()

var result *models_pkg.ImageResponse
result,_ = productImages.GetASingleProductImageData(productImageId)

```


### <a name="update_set_image_position"></a>![Method: ](https://apidocs.io/img/method.png ".productimages_pkg.UpdateSetImagePosition") UpdateSetImagePosition

> Allows for changing the image position in the list


```go
func (me *PRODUCTIMAGES_IMPL) UpdateSetImagePosition(
            body *models_pkg.ImagePosition,
            productImageId *string)(*models_pkg.ImageResponse,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| productImageId |  ``` Optional ```  | TODO: Add a parameter description |


#### Example Usage

```go
bodyValue := []byte("{  \"position\": 1}")
var body *models_pkg.ImagePosition
json.Unmarshal(bodyValue,&body)
productImageId := "product_image_id"

var result *models_pkg.ImageResponse
result,_ = productImages.UpdateSetImagePosition(body, productImageId)

```


### <a name="delete_a_product_image"></a>![Method: ](https://apidocs.io/img/method.png ".productimages_pkg.DeleteAProductImage") DeleteAProductImage

> Deletes the product_image with the requested `id`.


```go
func (me *PRODUCTIMAGES_IMPL) DeleteAProductImage(productImageId *string)(,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productImageId |  ``` Optional ```  | TODO: Add a parameter description |


#### Example Usage

```go
productImageId := "product_image_id"

var result 
result,_ = productImages.DeleteAProductImage(productImageId)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="producttypes_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".producttypes_pkg") producttypes_pkg

### Get instance

Factory for the ``` PRODUCTTYPES ``` interface can be accessed from the package producttypes_pkg.

```go
productTypes := producttypes_pkg.NewPRODUCTTYPES()
```

### <a name="list_product_types"></a>![Method: ](https://apidocs.io/img/method.png ".producttypes_pkg.ListProductTypes") ListProductTypes

> Returns a paginated list of product types.


```go
func (me *PRODUCTTYPES_IMPL) ListProductTypes()(*models_pkg.ProductTypeCollection,error)
```

#### Example Usage

```go

var result *models_pkg.ProductTypeCollection
result,_ = productTypes.ListProductTypes()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="registers_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".registers_pkg") registers_pkg

### Get instance

Factory for the ``` REGISTERS ``` interface can be accessed from the package registers_pkg.

```go
registers := registers_pkg.NewREGISTERS()
```

### <a name="list_registers"></a>![Method: ](https://apidocs.io/img/method.png ".registers_pkg.ListRegisters") ListRegisters

> Returns a paginated list of registers.


```go
func (me *REGISTERS_IMPL) ListRegisters()(*models_pkg.RegisterCollection,error)
```

#### Example Usage

```go

var result *models_pkg.RegisterCollection
result,_ = registers.ListRegisters()

```


### <a name="get_a_single_register"></a>![Method: ](https://apidocs.io/img/method.png ".registers_pkg.GetASingleRegister") GetASingleRegister

> Returns a single register with the requested `id`.


```go
func (me *REGISTERS_IMPL) GetASingleRegister(registerId uuid.UUID)(*models_pkg.RegisterCollection,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| registerId |  ``` Required ```  | Valid register `id`. |


#### Example Usage

```go
registerId := uuid.NewV4()

var result *models_pkg.RegisterCollection
result,_ = registers.GetASingleRegister(registerId)

```


[Back to List of Controllers](#list_of_controllers)

## <a name="tags_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".tags_pkg") tags_pkg

### Get instance

Factory for the ``` TAGS ``` interface can be accessed from the package tags_pkg.

```go
tags := tags_pkg.NewTAGS()
```

### <a name="list_tags"></a>![Method: ](https://apidocs.io/img/method.png ".tags_pkg.ListTags") ListTags

> Returns a collection of tags.


```go
func (me *TAGS_IMPL) ListTags()(*models_pkg.TagCollection,error)
```

#### Example Usage

```go

var result *models_pkg.TagCollection
result,_ = tags.ListTags()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="sales_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".sales_pkg") sales_pkg

### Get instance

Factory for the ``` SALES ``` interface can be accessed from the package sales_pkg.

```go
sales := sales_pkg.NewSALES()
```

### <a name="list_sales"></a>![Method: ](https://apidocs.io/img/method.png ".sales_pkg.ListSales") ListSales

> Returns a paginated list of Sales.


```go
func (me *SALES_IMPL) ListSales()(*models_pkg.SaleCollection,error)
```

#### Example Usage

```go

var result *models_pkg.SaleCollection
result,_ = sales.ListSales()

```


[Back to List of Controllers](#list_of_controllers)

## <a name="suppliers_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".suppliers_pkg") suppliers_pkg

### Get instance

Factory for the ``` SUPPLIERS ``` interface can be accessed from the package suppliers_pkg.

```go
suppliers := suppliers_pkg.NewSUPPLIERS()
```

### <a name="list_suppliers"></a>![Method: ](https://apidocs.io/img/method.png ".suppliers_pkg.ListSuppliers") ListSuppliers

> Returns a paginated list of suppliers.


```go
func (me *SUPPLIERS_IMPL) ListSuppliers()(*models_pkg.SupplierCollection,error)
```

#### Example Usage

```go

var result *models_pkg.SupplierCollection
result,_ = suppliers.ListSuppliers()

```


[Back to List of Controllers](#list_of_controllers)



