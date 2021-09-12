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
// isAuth error occure
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

// autorization error occure
# Query posts
query{
  posts {
    posts{
      _id
      title
      content
      creator {
        name
      }
      createdAt
    }
    totalPosts
  }
}