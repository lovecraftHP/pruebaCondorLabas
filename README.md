# pruebaCondorLabas
This repository was created in order to upload the technical test imposed by condorLabs.
The test consisted of making an Amazon or Mercadolibre marketplace, which had the following requirements:
1. List of Products
2. Search Products
3. Product Detail
4. Add Products to the Shopping Cart
5. Shopping Cart Detail
6. Remove Products from the Shopping Cart
7. Display the Products by Category

## Tecnologies used
The development of this application was done in the ubuntu 18.04(x64) OS, also used:
* **Angular CLI**: 8.2.2
* **Node**: 10.16.2 (npm: '6.11.1')
* **mongodb**: db version v4.2.0

# FrontEnd
In the frontend part, the latest version of angular was used, so far it is 8, the libraries that were used were:
* **NgModule**:for two-way data manipulation
* **HttpClient**:To make requests to our backend, HttpHeaders was also used, for the correct configuration of the headers
* **ReactiveFormsModule,FormsModule** :for data manipulation and forms validation
* **ShoppingCartModule**: for the implementation of a shopping cart
to run the frontend part correctly, unzip the "front.zip" file in any folder, then open a terminal inside that folder and execute the command ***npm install*** this will install the dependencies that are inside the folder file **package.json**.
You could also create a new project using the ***ng new project*** command and when you finish copying and replacing the "front.zip" files inside the new project folder (I recommend the first one, this second way can result in mistakes).

## Routes
In the app-routing.module.ts file, the following routes are found
* '': Home
* 'create': create a new product
* 'search/:search', search a product by its name
* 'category/:category', search products by category
* 'edit/:id', update a product
* 'xx', a route to handle errors, would be 404, by default redirects to home

# Backend
the part of the backend was made with NodeJS, using the following libraries to facilitate the development:
* **express**:for the development of the Rest API
* **body-parser**:to convert requests to json objects
* **connect-multiparty**: to facilitate the upload of files to the server
* **mongoose** : to facilitate the connection and manipulation of mongodb database data
to run the Backend part correctly, unzip the "front.zip" file in any folder, then open a terminal inside that folder and execute the command ***npm install*** this will install the dependencies that are inside the folder file.

## Controllers
there are 2 controllers inside this folder.
* **category**: who has the methods to get all the categories saved in the DB
* **product** : who has all the methods, for add,edit,delete,list,details and search a product

## Models
both have the respective structure that the category and product objects must carry
there are 2 models:
* **category**: It has a title and an id
* **product**: it has a name,description, smallDescription(future implementation), images(future Implementation), smallImage, price, count, category

## Services
it has a file called **cartService.js** which was for an implementation of a shopping cart from node.

## Uploads
This is the place where all the uploaded images of the products will go
