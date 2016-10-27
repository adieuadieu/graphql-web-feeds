# GraphQL Web Feeds
Reconciling old shit with new shit; Query web feeds (RSS, Atom, and RDF) with GraphQL

## Contents
1. [What is it?](#what-is-it)
1. [Try it](#try-it)
1. [Installation](#installation)
1. [Querying](#querying)
1. [Configuration](#configuration)
1. [Testing](#testing)
1. [Troubleshooting](#troubleshooting)

## What is it?

Sometimes you gotta make use of an RSS/Atom/RDF web feed. `graphql-web-feeds` aims to make it easy to do that in your GraphQL API.

## Try it

Demo Todo :-(

## Features / Roadmap-todo

- [ ] make it do something
- [ ] cache
- [ ] aggregate multiple feeds into one, sorted by date (at the detriment of speed)
- [ ] offer an Atom/RDF/RSS Interface type ?

## Installation

The package makes the assumption that, because you're using GraphQL, you're probably also using ES6+ and therefore your project handles any necessary transpilation, when required.

First, install the package:

```bash
npm install graphql-web-feeds --save
```

Then, add it to your project's GraphQL schema:

```js
import { RssObjectType } from 'web-feeds-graphql';

```

## Querying

```graphql
query {
  waitButWhy: feed(url: "http://waitbutwhy.com/feed") {
    title
    link
    description
    items {
      title
      link
      description
    }
  }
}
```

## Configuration

Todo

## Testing

```bash
git clone https://github.com/adieuadieu/graphql-web-feeds.git
cd graphql-web-feeds
npm test
```

## FAQ / Troubleshooting

<details>
  <summary>Todo?</summary>
  Todo.
</details>
