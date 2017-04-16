# react-native-apollo-instagram-example

* [React Native](https://facebook.github.io/react-native/): Javascript framework for building native mobile apps with [React](https://facebook.github.io/react/)
* [Apollo Client](https://github.com/apollographql/apollo-client): Fully-featured, production ready caching GraphQL client
* [Graphcool](https://www.graph.cool): Flexible backend platform combining GraphQL + AWS Lambda

## Example ([Live demo]() & [GraphQL Playground](https://api.graph.cool/simple/v1/instagram-example))

> TODO: GIF of final product

## Quickstart

For more information on how to get started [refer to the full react-native-apollo-instagram tutorial](https://www.graph.cool/docs/quickstart/react-native-apollo-instagram-example).

### 1. Clone example repository

```sh
git clone https://github.com/graphcool-examples/react-native-apollo-instagram-example.git
cd react-native-apollo-instagram-example
```

### 2. Create GraphQL API with [`graphcool`](https://www.npmjs.com/package/graphcool)

```sh
# Install Graphcool CLI
npm install -g graphcool

# Create a new project based on the Instagram schema
graphcool init --url graph.cool/schema/instagram 
```

This creates a GraphQL API for the following schema:

```graphql
type Post {
  description: String!
  imageUrl: String!
}
```

### 3. Connect the app with your GraphQL API

Copy the `Simple API` endpoint to `./src/root.js` as the `uri` argument in the `createNetworkInterface` call:

```js
// replace `__SIMPLE_API_ENDPOINT__` with the endpoint from the previous step
const networkInterface = createNetworkInterface({ uri: '__SIMPLE_API_ENDPOINT__' })
```

### 4. Install depdendencies & run locally

```sh
yarn install
yarn start # open http://localhost:3000 in your browser
```

## Next steps

* [Advanced GraphQL features](x)
* [Authentication & Permissions](x)
* [Implementing business logic with serverless functions](x)


## Help & Community [![Slack Status](https://slack.graph.cool/badge.svg)](https://slack.graph.cool)

Join our [Slack community](http://slack.graph.cool/) if you run into issues or have questions. We love talking to you!

![](http://i.imgur.com/5RHR6Ku.png)
