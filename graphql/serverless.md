# GraphQL in a Serverless World

## GraphQL

* Is a specification, like JSON
* GraphQL use types like REST uses resources
* Graph representation of types and their relationships
* Strongly typed
* Has queries and mutations (and subscriptions)
* Let's me describe the data in a helpfully complex way, showing relationships and types
* Allows for introspection of data
* Resolver, which is a server-side function that knows how to get a data type or accomplish a mutation
* GraphQL differs from SQL in that you can query other APIs, files, or databases

## Benefits and Considerations

### Benefits

* Improved data retrieval
* Great developer experience
* Excellent client libraries (Apollo)
* Lower bandwidth usage (request only what you need)

### Considerations

* New and unknown (compared to REST)
* Potential single point of failure, if you're using microservices unified by a GraphQL layer
* Potential for query abuse, though Query complexity warnings can abate this concern
* Obviates inherent REST capabilities, like caching unique URLs (always POSTing your query to a single endpoint)

## Demo App

Was dope.
