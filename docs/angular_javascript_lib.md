# Getting started

TODO: Add a description

## How to Build

The generated SDK requires AngularJS framework to work. If you do not already have angular downloaded, please go ahead and do it from [here](https://angularjs.org/).
If any of your models have `Date` or `Datetime` type fields or your endpoints have `Date`/`Datetime` type response, you will need to download and link [angular-moment](https://cdnjs.cloudflare.com/ajax/libs/angular-moment/1.0.1/angular-moment.min.js) and [moment.js](https://cdnjs.cloudflare.com/ajax/libs/moment.js/2.17.1/moment.min.js) with your project.

## How to Use

The following section describes how to use the generated SDK in an existing/new project.

### 1. Configure Angular and Generated SDK
Perform the following steps to configure angular and the SDK:
+ Make a `scripts` folder inside the root folder of the project. If you already have a `scripts` folder, skip to the next step.
+ Move the `angular.min.js` file inside the scripts folder. 
+ Move the `VendRESTAPI20Lib` folder inside the scripts folder.
+ If any of the Custom Types in your API have `Date`/`Datetime` type fields or any endpoint has `Date`/`Datetime` response, you will need to download angular-moment and moment.js. Move these 2 files into the `scripts` folder as well.

![folder-structure-image](https://apidocs.io/illustration/angularjs?step=folderStructure&workspaceFolder=Vend%20REST%20API%202.0-Angular&projectName=VendRESTAPI20Lib)

### 2. Open Project Folder
Open an IDE/Text Editor for JavaScript like Sublime Text. The basic workflow presented here is also applicable if you prefer using a different editor or IDE.  
Click on `File` and select `Open Folder`

Select the folder of your SDK and click on `Select Folder` to open it up in Sublime Text. The folder will become visible in the bar on the left.

![open-folder-image](https://apidocs.io/illustration/angularjs?step=openFolder&workspaceFolder=Vend%20REST%20API%202.0-Angular)

### 3. Create an Angular Application
Since Angular JS is used for client-side web development, in order to use the generated library, you will have to develop an application first.
If you already have an angular application, [skip to Step 6](#6-include-sdk-references-in-html-file). Otherwise, follow these steps to create one:

+ In the IDE, click on `File` and choose `New File` to create a new file.
+ Add the following starting code in the file:
```js
var app = angular.module('myApp', []);
app.controller('testController', function($scope) 
{

});
```
+ Save it with the name `app.js` in the `scripts` folder.


### 4. Create HTML File
Skip to the next step if you are working with an existing project and already have an html file. Otherwise follow the steps to create one:
+ Inside the IDE, right click on the project folder name and select the `New File` option to create a new test file.
+ Save it with an appropriate name such as `index.html` in the root of your project folder.
`index.html` should look like this:
```html
<!DOCTYPE html>
<html>
<head>
	<title>Angular Project</title>
	<script></script>
</head>

<body>
</body>

</html>
```

![initial-html-code-image](https://apidocs.io/illustration/angularjs?step=initialCode&workspaceFolder=Vend%20REST%20API%202.0-Angular)

### 5. Including links to Angular in HTML file
Your HTML file needs to have a link to `angular.min.js` file to use Angular-JS. Add the link using `script` tags inside the `head` section of `index.html` like:
```html
<script src="scripts/angular.min.js" ></script>
```
If any of the Custom Types that you have defined have `Date`/`Datetime` type fields or any endpoint has `Date`/`Datetime` response, you will also need to link to angular-moment and moment.js like:
```html
<script src="scripts/angular.min.js" ></script>
<script src="scripts/moment.min.js" ></script>
<script src="scripts/angular-moment.min.js" ></script>
```

### 6. Include SDK references in HTML file
Import the reference to the generated SDK files inside your html file like:
```html
<head>
    ...
    <!-- Helper files -->
    <script src="scripts/VendRESTAPI20Lib/Module.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Configuration.js"></script>
    <script src="scripts/VendRESTAPI20Lib/ModelFactory.js"></script>
    <script src="scripts/VendRESTAPI20Lib/ObjectMapper.js"></script>
    <script src="scripts/VendRESTAPI20Lib/APIHelper.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Http/Client/HttpContext.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Http/Client/RequestClient.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Http/Request/HttpRequest.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Http/Response/HttpResponse.js"></script>

    <!-- API Controllers -->
    <script src="scripts/VendRESTAPI20Lib/Controllers/BaseController.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Controllers/BrandsController.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Controllers/CustomersController.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Controllers/CustomerGroupsController.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Controllers/ConsignmentsController.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Controllers/InventoryController.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Controllers/OutletsController.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Controllers/PriceBooksController.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Controllers/PriceBookProductsController.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Controllers/ProductsController.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Controllers/ProductImagesController.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Controllers/ProductTypesController.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Controllers/RegistersController.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Controllers/TagsController.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Controllers/SalesController.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Controllers/SuppliersController.js"></script>


    <!-- Models -->
    <script src="scripts/VendRESTAPI20Lib/Models/BaseModel.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/BrandBase.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/Brand.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/BrandResponse.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/BrandCollection.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/CustomerBase.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/Customer.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/CustomerResponse.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/CustomerCollection.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/CustomerGroupBase.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/CustomerGroup.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/CustomerGroupResponse.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/CustomerGroupCollection.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/ConsignmentBase.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/Consignment.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/ConsignmentResponse.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/ConsignmentCollection.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/InventoryBase.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/Inventory.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/InventoryResponse.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/InventoryCollection.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/OutletBase.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/Outlet.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/OutletResponse.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/OutletCollection.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/PriceBookBase.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/PriceBook.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/PriceBookResponse.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/PriceBookCollection.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/PriceBookProductBase.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/PriceBookProduct.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/PriceBookProductCollection.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/ProductBase.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/ProductTypeSample.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/SupplierSample.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/BrandSample.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/VariantOptionSample1.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/CategorySample1.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/Product.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/ImageSample.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/ProductResponse.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/ProductCollection.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/VariantOption.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/ImageBase.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/Image.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/ImageResponse.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/ImagePosition.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/ProductTypeBase.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/ProductType.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/ProductTypeResponse.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/ProductTypeCollection.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/RegisterBase.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/Register.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/RegisterResponse.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/RegisterCollection.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/TagBase.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/Tag.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/TagResponse.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/TagCollection.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/SaleBase.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/LineItem.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/LineItemBase.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/TaxComponent.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/Payment.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/PaymentBase.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/Sale.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/Tax.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/SaleResponse.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/SaleCollection.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/SupplierBase.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/Supplier.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/SupplierResponse.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/SupplierCollection.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/TimestampC.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/TimestampU.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/TimestampCU.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/TimestampCUD.js"></script>
    <script src="scripts/VendRESTAPI20Lib/Models/UploadAnImageRequest.js"></script>

    ...
</head>
```
> The `Module.js` file should be imported before the other files. After `Module.js`, `Configuration.js` should be imported.
> The `ModelFactory.js` file is needed by `ObjectMapper.js` file. The `ObjectMapper` in turn, is needed by `BaseController.js`.

### 7. Including link to `app.js` in HTML file
Link your `app.js` file to your `index.html` file like:
```html
<head>
	...
	<script src="scripts/app.js"></script>
</head>
```
> The link to app.js needs to be included at the very end of the head tag, after the SDK references have been added

### 8. Initializing the Angular App
You need to initialize your app and the controller associated with your view inside your `index.html` file. Do so like:
+ Add ng-app directive to initialize your app inside the `body` tag.
```html
<body ng-app="myApp">
```
+ Add ng-controller directive to initialize your controller and bind it with your view (`index.html` file).
```html
...
<body ng-app="myApp">
	<div ng-controller="testController">
		...
	</div>
	...
</body>
...
```

### 9. Consuming the SDK 
In order to use the generated SDK's modules, controllers and factories, the project needs to be added as a dependency in your angular app's module. This will be done inside the `app.js` file.
Add the dependency like this:

```js
var app = angular.module('myApp', ['VendRESTAPI20Lib']);
```
At this point, the SDK has been successfully included in your project. Further steps include using a service/factory from the generated SDK. To see working example of this, please head on [over here](#list-of-controllers) and choose any class to see its functions and example usage.  

### 10. Running The App
To run the app, simply open up the `index.html` file in a browser.

![app-running](https://apidocs.io/illustration/angularjs?step=appRunning)

## Initialization


The Angular Application can be initialized as following:
```JavaScript
var app = angular.module('myApp', [VendRESTAPI20Lib]);
// now controllers/services can be created which import
// the factories provided by the sdk
```
### Authentication
In order to setup authentication and initialization of the Angular App, you need the following information.

| Parameter | Description |
|-----------|-------------|
| oAuthAccessToken | OAuth 2.0 Access Token |



```JavaScript
var app = angular.module('myApp', [VendRESTAPI20Lib]);
app.factory('config', function($scope, Configuration) 
{
    return {
        setConfigVars: function() {
            // Configuration parameters and credentials
            Configuration.oAuthAccessToken = 'oAuthAccessToken'; // OAuth 2.0 Access Token
            
        }
    };
});
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

The singleton instance of the ``` BrandsController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, BrandsController, BrandCollection){
	});
```

### <a name="list_brands"></a>![Method: ](https://apidocs.io/img/method.png ".BrandsController.listBrands") listBrands

> Returns a paginated list of brands.


```javascript
function listBrands()
```

#### Example Usage

```javascript


	app.controller("testController", function($scope, BrandsController, BrandCollection){


		var result = BrandsController.listBrands();
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="customers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CustomersController") CustomersController

### Get singleton instance

The singleton instance of the ``` CustomersController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, CustomersController, CustomerCollection, CustomerResponse){
	});
```

### <a name="list_customers"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.listCustomers") listCustomers

> Returns a paginated list of customers.


```javascript
function listCustomers()
```

#### Example Usage

```javascript


	app.controller("testController", function($scope, CustomersController, CustomerCollection){


		var result = CustomersController.listCustomers();
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="create_a_new_customer"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.createANewCustomer") createANewCustomer

> Creates a new customer.


```javascript
function createANewCustomer(body)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, CustomersController, CustomerResponse){
        var body = new CustomerBase({  "customer_code": "Tony-QKG3",  "customer_group_id": "b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4",  "enable_loyalty": true,  "first_name": "Tony",  "last_name": "Stark",  "email": "ironman@avengers.com",  "note": "",  "gender": "M",  "date_of_birth": "1963-03-03",  "company_name": "Stark Inc.",  "phone": "",  "mobile": "",  "fax": "",  "twitter": "",  "website": "",  "physical_address_1": "",  "physical_address_2": "",  "physical_suburb": "",  "physical_city": "",  "physical_postcode": "",  "physical_state": "",  "physical_country_id": "US",  "postal_address_1": "",  "postal_address_2": "",  "postal_suburb": "",  "postal_city": "",  "postal_postcode": "",  "postal_state": "",  "postal_country_id": "",  "custom_field_1": "",  "custom_field_2": "",  "custom_field_3": "",  "custom_field_4": ""});


		var result = CustomersController.createANewCustomer(body);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="get_a_single_customer"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.getASingleCustomer") getASingleCustomer

> Returns a single customer with a requested `id`.


```javascript
function getASingleCustomer(customerId)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |



#### Example Usage

```javascript


	app.controller("testController", function($scope, CustomersController, CustomerResponse){
        var customerId = uniqid();


		var result = CustomersController.getASingleCustomer(customerId);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="update_a_customer"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.updateACustomer") updateACustomer

> Updates editable fields for the customer with the requested `id`.


```javascript
function updateACustomer(customerId, body)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, CustomersController, CustomerResponse){
        var customerId = uniqid();
        var body = new CustomerBase({"key":"value"});


		var result = CustomersController.updateACustomer(customerId, body);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="delete_a_customer"></a>![Method: ](https://apidocs.io/img/method.png ".CustomersController.deleteACustomer") deleteACustomer

> Deletes the customer with the requested `id`.


```javascript
function deleteACustomer(customerId)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| customerId |  ``` Required ```  | Valid customer `id`. |



#### Example Usage

```javascript


	app.controller("testController", function($scope, CustomersController){
        var customerId = uniqid();


		var result = CustomersController.deleteACustomer(customerId);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="customer_groups_controller"></a>![Class: ](https://apidocs.io/img/class.png ".CustomerGroupsController") CustomerGroupsController

### Get singleton instance

The singleton instance of the ``` CustomerGroupsController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, CustomerGroupsController, CustomerGroupCollection){
	});
```

### <a name="list_customer_groups"></a>![Method: ](https://apidocs.io/img/method.png ".CustomerGroupsController.listCustomerGroups") listCustomerGroups

> Returns a paginated list of customer groups.


```javascript
function listCustomerGroups()
```

#### Example Usage

```javascript


	app.controller("testController", function($scope, CustomerGroupsController, CustomerGroupCollection){


		var result = CustomerGroupsController.listCustomerGroups();
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="consignments_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ConsignmentsController") ConsignmentsController

### Get singleton instance

The singleton instance of the ``` ConsignmentsController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, ConsignmentsController, ConsignmentCollection, ConsignmentResponse){
	});
```

### <a name="list_consignments"></a>![Method: ](https://apidocs.io/img/method.png ".ConsignmentsController.listConsignments") listConsignments

> Returns a paginated list of consignments.


```javascript
function listConsignments()
```

#### Example Usage

```javascript


	app.controller("testController", function($scope, ConsignmentsController, ConsignmentCollection){


		var result = ConsignmentsController.listConsignments();
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="get_a_single_consignment"></a>![Method: ](https://apidocs.io/img/method.png ".ConsignmentsController.getASingleConsignment") getASingleConsignment

> Returns a single consignment with the requested `id`.


```javascript
function getASingleConsignment(consignmentId)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| consignmentId |  ``` Required ```  | Valid consignment `id`. |



#### Example Usage

```javascript


	app.controller("testController", function($scope, ConsignmentsController, ConsignmentResponse){
        var consignmentId = uniqid();


		var result = ConsignmentsController.getASingleConsignment(consignmentId);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="inventory_controller"></a>![Class: ](https://apidocs.io/img/class.png ".InventoryController") InventoryController

### Get singleton instance

The singleton instance of the ``` InventoryController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, InventoryController, InventoryCollection){
	});
```

### <a name="list_inventory_records"></a>![Method: ](https://apidocs.io/img/method.png ".InventoryController.listInventoryRecords") listInventoryRecords

> Returns a paginated list of Inventory records.


```javascript
function listInventoryRecords()
```

#### Example Usage

```javascript


	app.controller("testController", function($scope, InventoryController, InventoryCollection){


		var result = InventoryController.listInventoryRecords();
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="outlets_controller"></a>![Class: ](https://apidocs.io/img/class.png ".OutletsController") OutletsController

### Get singleton instance

The singleton instance of the ``` OutletsController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, OutletsController, OutletCollection){
	});
```

### <a name="list_outlets"></a>![Method: ](https://apidocs.io/img/method.png ".OutletsController.listOutlets") listOutlets

> Returns a collection of outlets.


```javascript
function listOutlets()
```

#### Example Usage

```javascript


	app.controller("testController", function($scope, OutletsController, OutletCollection){


		var result = OutletsController.listOutlets();
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="get_a_single_outlet"></a>![Method: ](https://apidocs.io/img/method.png ".OutletsController.getASingleOutlet") getASingleOutlet

> Returns a single outlet with the requested `id`.


```javascript
function getASingleOutlet(outletId)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| outletId |  ``` Required ```  | Valid Outlet `id`. |



#### Example Usage

```javascript


	app.controller("testController", function($scope, OutletsController, OutletCollection){
        var outletId = uniqid();


		var result = OutletsController.getASingleOutlet(outletId);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="price_books_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PriceBooksController") PriceBooksController

### Get singleton instance

The singleton instance of the ``` PriceBooksController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, PriceBooksController, PriceBookCollection, PriceBookResponse){
	});
```

### <a name="list_price_books"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBooksController.listPriceBooks") listPriceBooks

> Returns a paginated list of price books


```javascript
function listPriceBooks()
```

#### Example Usage

```javascript


	app.controller("testController", function($scope, PriceBooksController, PriceBookCollection){


		var result = PriceBooksController.listPriceBooks();
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="create_a_price_book"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBooksController.createAPriceBook") createAPriceBook

> Creates a new price book.


```javascript
function createAPriceBook(body)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, PriceBooksController, PriceBookResponse){
        var body = new PriceBookBase({  "name": "Test",  "valid_from": "2018-01-01",  "valid_to": "2019-01-01",  "restrict_to_platform_key": "1",  "customer_group_id": "b1ca8902-f019-11e3-a0f5-b8ca3a64f8f4",  "outlet_id": ""});


		var result = PriceBooksController.createAPriceBook(body);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="get_a_single_price_book"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBooksController.getASinglePriceBook") getASinglePriceBook

> Returns a single price book with a requested `id`


```javascript
function getASinglePriceBook(priceBookId)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| priceBookId |  ``` Required ```  | Valid price book `id`. |



#### Example Usage

```javascript


	app.controller("testController", function($scope, PriceBooksController, PriceBookResponse){
        var priceBookId = uniqid();


		var result = PriceBooksController.getASinglePriceBook(priceBookId);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="price_book_products_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PriceBookProductsController") PriceBookProductsController

### Get singleton instance

The singleton instance of the ``` PriceBookProductsController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, PriceBookProductsController, PriceBookProductCollection){
	});
```

### <a name="list_price_book_products"></a>![Method: ](https://apidocs.io/img/method.png ".PriceBookProductsController.listPriceBookProducts") listPriceBookProducts

> Returns a paginated list of price book products.


```javascript
function listPriceBookProducts()
```

#### Example Usage

```javascript


	app.controller("testController", function($scope, PriceBookProductsController, PriceBookProductCollection){


		var result = PriceBookProductsController.listPriceBookProducts();
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="products_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductsController") ProductsController

### Get singleton instance

The singleton instance of the ``` ProductsController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, ProductsController, ProductCollection, ProductResponse, InventoryCollection, ImageResponse){
	});
```

### <a name="list_products"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.listProducts") listProducts

> Returns a paginated list of products.


```javascript
function listProducts()
```

#### Example Usage

```javascript


	app.controller("testController", function($scope, ProductsController, ProductCollection){


		var result = ProductsController.listProducts();
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="get_a_single_product"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.getASingleProduct") getASingleProduct

> Returns a single product object with a given `id`.


```javascript
function getASingleProduct(productId)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productId |  ``` Required ```  | Valid product `id`. |



#### Example Usage

```javascript


	app.controller("testController", function($scope, ProductsController, ProductResponse){
        var productId = uniqid();


		var result = ProductsController.getASingleProduct(productId);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="get_inventory_data_for_a_single_product"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.getInventoryDataForASingleProduct") getInventoryDataForASingleProduct

> Returns inventory data for a single product in all the outlets.


```javascript
function getInventoryDataForASingleProduct(productId)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productId |  ``` Required ```  | Valid product `id`. |



#### Example Usage

```javascript


	app.controller("testController", function($scope, ProductsController, InventoryCollection){
        var productId = uniqid();


		var result = ProductsController.getInventoryDataForASingleProduct(productId);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="upload_an_image"></a>![Method: ](https://apidocs.io/img/method.png ".ProductsController.uploadAnImage") uploadAnImage

> Upload a binary file with an image to be used for a product.


```javascript
function uploadAnImage(body, productId)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| productId |  ``` Optional ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, ProductsController, ImageResponse){
        var body = new UploadAnImageRequest({"key":"value"});
        var productId = product_id;


		var result = ProductsController.uploadAnImage(body, productId);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="product_images_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductImagesController") ProductImagesController

### Get singleton instance

The singleton instance of the ``` ProductImagesController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, ProductImagesController, ImageResponse){
	});
```

### <a name="get_a_single_product_image_data"></a>![Method: ](https://apidocs.io/img/method.png ".ProductImagesController.getASingleProductImageData") getASingleProductImageData

> Returns the metadata for a single product image with a given `id`.
> This method is useful for checking the status of an image after it was uploaded.


```javascript
function getASingleProductImageData(productImageId)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productImageId |  ``` Required ```  | Valid product `id`. |



#### Example Usage

```javascript


	app.controller("testController", function($scope, ProductImagesController, ImageResponse){
        var productImageId = uniqid();


		var result = ProductImagesController.getASingleProductImageData(productImageId);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="update_set_image_position"></a>![Method: ](https://apidocs.io/img/method.png ".ProductImagesController.updateSetImagePosition") updateSetImagePosition

> Allows for changing the image position in the list


```javascript
function updateSetImagePosition(body, productImageId)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |
| productImageId |  ``` Optional ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, ProductImagesController, ImageResponse){
        var body = new ImagePosition({  "position": 1});
        var productImageId = product_image_id;


		var result = ProductImagesController.updateSetImagePosition(body, productImageId);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="delete_a_product_image"></a>![Method: ](https://apidocs.io/img/method.png ".ProductImagesController.deleteAProductImage") deleteAProductImage

> Deletes the product_image with the requested `id`.


```javascript
function deleteAProductImage(productImageId)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| productImageId |  ``` Optional ```  | TODO: Add a parameter description |



#### Example Usage

```javascript


	app.controller("testController", function($scope, ProductImagesController){
        var productImageId = product_image_id;


		var result = ProductImagesController.deleteAProductImage(productImageId);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="product_types_controller"></a>![Class: ](https://apidocs.io/img/class.png ".ProductTypesController") ProductTypesController

### Get singleton instance

The singleton instance of the ``` ProductTypesController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, ProductTypesController, ProductTypeCollection){
	});
```

### <a name="list_product_types"></a>![Method: ](https://apidocs.io/img/method.png ".ProductTypesController.listProductTypes") listProductTypes

> Returns a paginated list of product types.


```javascript
function listProductTypes()
```

#### Example Usage

```javascript


	app.controller("testController", function($scope, ProductTypesController, ProductTypeCollection){


		var result = ProductTypesController.listProductTypes();
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="registers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".RegistersController") RegistersController

### Get singleton instance

The singleton instance of the ``` RegistersController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, RegistersController, RegisterCollection){
	});
```

### <a name="list_registers"></a>![Method: ](https://apidocs.io/img/method.png ".RegistersController.listRegisters") listRegisters

> Returns a paginated list of registers.


```javascript
function listRegisters()
```

#### Example Usage

```javascript


	app.controller("testController", function($scope, RegistersController, RegisterCollection){


		var result = RegistersController.listRegisters();
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



### <a name="get_a_single_register"></a>![Method: ](https://apidocs.io/img/method.png ".RegistersController.getASingleRegister") getASingleRegister

> Returns a single register with the requested `id`.


```javascript
function getASingleRegister(registerId)
```
#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| registerId |  ``` Required ```  | Valid register `id`. |



#### Example Usage

```javascript


	app.controller("testController", function($scope, RegistersController, RegisterCollection){
        var registerId = uniqid();


		var result = RegistersController.getASingleRegister(registerId);
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="tags_controller"></a>![Class: ](https://apidocs.io/img/class.png ".TagsController") TagsController

### Get singleton instance

The singleton instance of the ``` TagsController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, TagsController, TagCollection){
	});
```

### <a name="list_tags"></a>![Method: ](https://apidocs.io/img/method.png ".TagsController.listTags") listTags

> Returns a collection of tags.


```javascript
function listTags()
```

#### Example Usage

```javascript


	app.controller("testController", function($scope, TagsController, TagCollection){


		var result = TagsController.listTags();
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="sales_controller"></a>![Class: ](https://apidocs.io/img/class.png ".SalesController") SalesController

### Get singleton instance

The singleton instance of the ``` SalesController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, SalesController, SaleCollection){
	});
```

### <a name="list_sales"></a>![Method: ](https://apidocs.io/img/method.png ".SalesController.listSales") listSales

> Returns a paginated list of Sales.


```javascript
function listSales()
```

#### Example Usage

```javascript


	app.controller("testController", function($scope, SalesController, SaleCollection){


		var result = SalesController.listSales();
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)

## <a name="suppliers_controller"></a>![Class: ](https://apidocs.io/img/class.png ".SuppliersController") SuppliersController

### Get singleton instance

The singleton instance of the ``` SuppliersController ``` class can be accessed via Dependency Injection.

```js
	app.controller("testController", function($scope, SuppliersController, SupplierCollection){
	});
```

### <a name="list_suppliers"></a>![Method: ](https://apidocs.io/img/method.png ".SuppliersController.listSuppliers") listSuppliers

> Returns a paginated list of suppliers.


```javascript
function listSuppliers()
```

#### Example Usage

```javascript


	app.controller("testController", function($scope, SuppliersController, SupplierCollection){


		var result = SuppliersController.listSuppliers();
        //Function call returns a promise
        result.then(function(success){
			//success case
			//getting context of response
			console.log(success.getContext());
		},function(err){
			//failure case
		});

	});
```



[Back to List of Controllers](#list_of_controllers)



