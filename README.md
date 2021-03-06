# graphql-template-basic-typescript

![](https://imgur.com/eMpNw0e.png)

Basic boilerplate for a scalable, production-ready GraphQL gateway server built in TypeScript.

## Features

* Database (via [Graphcool](https://graph.cool))
* Foundational base for new GraphQL servers

## Getting started

#### Requirements

* Node 8 (or higher)
* Graphcool CLI (Get it via `npm i -g graphcool@alpha`)
* GraphQL CLI (Get it via `npm i -g graphql-cli@beta`)
* Optional: GraphQL Playground desktop app (Download [here](https://github.com/graphcool/graphql-playground/releases))

#### Setup your project

Via `graphql-cli`

```sh
# 1. From the root directory of choice execute:
graphql create [project-name]

# 2. Choose the "Basic (TypeScript, DB)" option

# 3. Navigate to the new project
cd [project-name]

# 4. Deploy the Graphcool database
graphcool deploy
```

By cloning this repository

```sh
# 1. Clone the repository
git clone http://github.com/DevanB/graphql-template-basic-typescript

# 2. Navigate to the new project
cd [project-name]

# 3. Deploy the Graphcool database
graphcool deploy
```

#### Launch the local server

```sh
# Start server (runs on http://localhost:4000)
yarn start

# Open Playground to explore GraphQL API
yarn playground
```

## Docs

### Commands

* `yarn start` starts GraphQL server
* `yarn debug` starts GraphQL server in debug mode (open [chrome://inspect/#devices](chrome://inspect/#devices) to debug)
* `yarn playground` opens the GraphQL Playground
* `yarn build` builds the application
* `yarn deploy` deploys GraphQL server to [`now`](https://now.sh)

### Project Overview
#### `/`
- [`.graphqlconfig.yml`](https://github.com/graphcool/graphql-boilerplate/blob/master/.graphqlconfig.yml) GraphQL Config file containing the endpoints and schema configuration. Used by the [`graphql-cli`](https://github.com/graphcool/graphql-cli) and the [GraphQL Playground](https://github.com/graphcool/graphql-playground). See [graphql-config](https://github.com/graphcool/graphql-config) for more information.

#### `/database`
- [`/database/datamodel.graphql`](https://github.com/graphcool/graphql-boilerplate/blob/master/database/datamodel.graphql) contains the Database model that you define
- [`/database/schema.graphql`](https://github.com/graphcool/graphql-boilerplate/blob/master/database/schema.graphql) contains the database API that is being generated based on your `datamodel.graphql`

#### `/src`
- [`/src/schema.graphql`](https://github.com/graphcool/graphql-boilerplate/blob/master/src/schema.graphql) contains the GraphQL API of your application that is exposed to the world
- [`/src/index.ts`](https://github.com/graphcool/graphql-boilerplate/blob/master/src/index.ts) is the entry point of your application, defining the resolvers and starting the [`graphql-yoga`](https://github.com/graphcool/graphql-yoga) server.

## Community

Graphcool has a community of thousands of amazing developers and contributors. Welcome, please join us! 👋

* [Forum](https://www.graph.cool/forum)
* [Slack](https://slack.graph.cool/)
* [Stackoverflow](https://stackoverflow.com/questions/tagged/graphcool)
* [Twitter](https://twitter.com/graphcool)
* [Facebook](https://www.facebook.com/GraphcoolHQ)
* [Meetup](https://www.meetup.com/graphql-berlin)
* [Email](hello@graph.cool)

## Contributing

Your feedback is **very helpful**, please share your opinion and thoughts!
