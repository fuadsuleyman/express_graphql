# How to run

- npm start 


# How to test

- Run server
- Go to http://localhost:8080/graphql
- Run query

# Mutation signup
mutation {
  createUser(userInput: {email: "fuadsuli@mail.com", name: "Fuad", password: "123456"}) {
    _id
    email
  }
}

# Mutation createPost
mutation {
  createPost(postInput: {title: "test", content: "test", imageUrl: "some url"}) {
    _id
    title
  }
}


# Query login
query{
  login(email: "fuli@gmail.com", password: "123456") {
    token
    userId
  }
}