# Postman-Newman-GHactions
This is an enhanced repository as a task
- <a href="https://github.com/WannaBeDream/Postman-newman-ghActions"> Task repositiry link </a>

## Install
To run on the mock server
```git clone ```
Then install dipendences
```npm i```

## Run in Postman
1. Run the mock server ```npm run tern-on-api```
2. Import the `store.postman_collection.json` file into Postman
3. Open the "Store" collection
4. CLick the "send" button to run tests

## Run by Neman
Enter in the terminal ```npx newman run store.postman_collection.json```

### Overview of local server testing
Routes `/products`, `/orders` and `/users`. Below is a table of supported operations with `products` as example resource. The same operations are also supports for `orders/` and `users/`.

| VERB     |Route          | Input      | Output             |
|----------|---------------|------------|--------------------|
| GET      | /products     | *None*     | **Array**          |
| GET      | /products/:id |  **e.g 3** | **Object**         |
| POST     | /products     | **object** | **Created object** |
| PUT      | /products     | **object** | **Updated object** |
| DELETE   | /products/:id | **e.g 3**  | **Deleted object** |


5. Upload `store.collection.json` in Postman app. (skip this exhibit in case you decide to use another public API ) 
6. Make some integration tests in Postman, could be status code/JSON check and so on. ( in case with another API - write tests based on another one).

Examples:
- Test pagination, by way like `http://localhost:3000/users?page=1&pageSize=2`. 
- Test sorting, by way like `http://localhost:3000/users?sortOrder=ASC&sortKey=firstName`. You can sort an any resource response using query parameters sortOrder and sortKey.
-  Test status code for REST API (200,400 and so on).
-  Test response time.
-  Test response thanks to json schema validation.
-  Try to follow `AAA` approach (arrange, act, assert).

7. Save new collection with your new integration tests with the same name as `store.collection.json`. ( in case with another API - another file name for json file)
8. Push to you github repo in main branch ( in case with local server - save local server as well )

###  GH actions practice
9. Add Github action to run `petstore.collection.json` in Github pages by <a href="https://www.linkedin.com/pulse/running-postman-collections-via-github-action-nirmala-jayasanka"> article </a> or use another GH action.
10. Check github actions for result.


You can use another API to perform  your testing instead of local store API and `store.collection.json`. 
- <a href="https://github.com/public-apis/public-apis"> Public API list </a>
