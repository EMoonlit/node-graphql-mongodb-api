# Fork de https://github.com/luizcalaca/node-graphql-mongodb-api
## TODO
- [ ] Abstrair e aplicar conceitos de GraphQL
- [ ] Fazer comparação com o uso de uma API RESTful com express semelhante e colher inputs de casos de uso
- [ ] Refatorar para typescript


# Blog API em GraphQL

Um aplicativo em GraphQL para gerenciar posts

#### How to run

```
git clone https://github.com/luizcalaca/node-graphql-mongodb-api.git
npm install
npm start
```

Access on: http://localhost/4000 and will be opened the GraphQL playground

#### Example on Playground

```
mutation CreatePost($post: PostInput) {
  createPost(post: $post) {
    name,
    comments {
      description
    }
  }
}
```

Using the below Headers:

```
{
  "post": {
    "name": "GraphQL vs REST",
    "comments": {
      "description": "That's difficult to discuss about"
    }
  }
}
```

We will post this:

```
{
  "data": {
    "createPost": {
      "name": "GraphQL vs REST",
      "comments": {
        "description": "That's difficult to discuss about"
      }
    }
  }
}
```
