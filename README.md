# Kayvee-rs
Kayvee is an in-memory key-value store written in Rust. It implements three methods: `GET`, `PUT`, and `DELETE` all of which are accessible via it's [GraphQL](https://kayvee.herokuapp.com/graphiql) endpoint.

## Methods
+ ### PUT
  ```graphql
    mutation {
      put(key: "name", value: "Michæl") {
        success
      }
    }
  ```
  ```json
    {
      "data": {
        "put": {
          "success": true
        }
      }
    }
  ```

+ ### GET
  ```graphql
    query {
      get(key: "name")
    }
  ```
  ```json
    {
      "data": {
        "get": "Michæl"
      }
    }
  ```

+ ### DELETE
  ```graphql
    mutation {
      delete(key: "name") {
        success
      }
    }
  ```
  ```json
    {
      "data": {
        "delete": {
          "success": true
        }
      }
    }
  ```

## Note
If you want to replicate this, remember to use the Heroku Rust buildpack here: https://github.com/emk/heroku-buildpack-rust.