# Bakery App – Auto1 Frontend Challenge
![bakery shop](https://static.vecteezy.com/system/resources/previews/002/045/877/large_2x/fancy-bakery-shop-with-trees-and-bike-vector.jpg)

## Context

The local bakery would like to extend its business by offering their products online. They approached you to help them build an app for this purpose.

This app should list all the different bakery products and needs to give the option to order them. 

Luckily the bakery provides an [API](#api-reference) as well as a [design](#design) for you to work with.

## Product Requirements

As a customer:

- [ ] I want to see a list of all products the bakery offers.
- [ ] For each product I want to see:
    - [ ] Product name
    - [ ] Product thumbnail
    - [ ] Product price
- [ ] For each product I want to be able: 
  - [ ] to select the amount I want to order
  - [ ] to not select more items than are available
- [ ] I want to see the total price of all my selected products.
- [ ] I want to see a "disabled" state if a product is out of stock.
- [ ] I want to see a success page once I ordered
- [ ] I want to be able to submit multiple orders

## Your Task

Create a React application that fulfills all requirements above, plus any nice-to-have requirements you wish to include.

For that, you will need to make requests to the API delivered in this repository.

If you are not able to implement a particular requirement, please provide a description of what and why you could not implement it.

For the layout of each page, please refer to the provided screens:

- [Index page](./screens/index.png)
- [Success page](./screens/success.png)

Font being used in these screens is [Montserrat](https://fonts.google.com/specimen/Montserrat) and can be embedded from Google Fonts.

## Tech Requirements

- React
- Bootstrap 3, 4 or 5
- Using any CSS preprocessor is a plus

## Instructions

- Build a clean and well-structured solution
- Send it to [frontend-marketing-challenge@auto1-group.com](mailto:frontend-marketing-challenge@auto1-group.com) as a zip container (please name is as A1G-FE-challenge-${your_name})

## API Reference

#### Get all items

```http
  GET /api/storage
```

- Returns an array `storage`
- Inside of `storage` are multiple objects with the following structure:

| Key | Type | Description |
| :-------- | :------- | :--- |
| `name` | `string` | Name of item |
| `stock` | `integer` | Number of items in stock |
| `price` | `number` | Price of item |

#### Post order

```http
  POST /api/order
```

- Expects an array `items`
- Inside of `items` one or multiple objects of the following structure are expected:

| Key | Type | Description |
| :--- | :--- | :--- |
| `name` | `string` | **Required**. name of item to order |
| `quantity` | `integer` | **Required**. quantity of item to order |

- the api will return status code 200 and `{message: 'success'}` if the order went through
- the api will return status code 400 and `{error: 'ERROR_MESSAGE', errorItem: 'ITEM_NAME'}` if the quantity is too high for a certain item

## Setup and run server
```
cd auto1-challenge
npm i
npm run start
```


## Setup and run frontend
```
cd auto1-challenge/client
npm i
npm run start
```


## Credits

Icons made by [Freepik](https://www.freepik.com)</a> from [https://www.flaticon.com/](www.flaticon.com)