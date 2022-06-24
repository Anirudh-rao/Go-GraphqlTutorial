# Go-GraphqlTutorial

A GraphQL server is able to receive requests in GraphQL Query Language format and return response in desired form. GraphQL is a query language for API so you can send queries and ask for what you need and exactly get that piece of data.

#### For this Project we will be using :

1. ```Go``` is a modern general purpose programming language designed by google; best known for it’s simplicity, concurrency and fast performance. It’s being used by big players in the industry like Google, Docker, Lyft and Uber. If you are new to golang you can start from golang tour to learn fundamentals.

2. [```gqlgen```](https://gqlgen.com/) is a library for creating GraphQL applications in Go.


In this tutorial we Implement a Hackernews GraphQL API clone with golang and gqlgen and learn about GraphQL fundamentals along the way.


### To Get Started :
1. Initialize the go mod file by running:
```go mod init github.com/[username]/hackernews```
2. Get the gqlgen package by running :
```go get github.com/99designs/gqlgen```
3. Now use gqlgen and intialize basic graphql project:
```go run github.com/99designs/gqlgen init```


Here is a description from gqlgen about the generated files:

1. ```gqlgen.yml``` — The gqlgen config file, knobs for controlling the generated code.
2. ```graph/generated/generated.go``` — The GraphQL execution runtime, the bulk of the generated code.
3. ```graph/model/models_gen.go``` — Generated models required to build the graph. Often you will override these with your own models. Still very useful for input types.
4. ```graph/schema.graphqls``` — This is the file where you will add GraphQL schemas.
5. ```graph/schema.resolvers.go``` — This is where your application code lives. generated.go will call into this to get the data the user has requested.
6. ```server.go``` — This is a minimal entry point that sets up an http.Handler to the generated GraphQL server. start the server with go run server.go and open your browser and you should see the graphql playground, So setup is right!