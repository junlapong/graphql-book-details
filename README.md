# GraphQL Java Spring Boot Example 

from: https://github.com/graphql-java/tutorials/tree/master/book-details

This is the source code for the [Getting started with GraphQL Java and Spring Boot](https://www.graphql-java.com/tutorials/getting-started-with-spring-boot/)

## Run

	./gradlew bootRun

## Try out the API

URL Endpoint: http://localhost:8080/graphql  

The easiest way to try out and explore a GraphQL API is to use a tool like [GraphQL Playground](https://github.com/prisma/graphql-playground). Download it and run it.

### Example Query

```graphql
query {
  bookById(id: "book-1") {
    id
    name
    pageCount
    author {
      firstName
      lastName
    }
  }
}
```

### Result

```json
{
  "data": {
    "bookById": {
      "id": "book-1",
      "name": "Harry Potter and the Philosopher's Stone",
      "pageCount": 223,
      "author": {
        "firstName": "Joanne",
        "lastName": "Rowling"
      }
    }
  }
}
```
