# Web Feeds GraphQL
Reconsiling old shit with new shit; Query web feeds (RSS, Atom, and RDF) with GraphQL

[![npm package](https://img.shields.io/npm/v/web-feeds-graphql.svg?style=flat-square)](https://www.npmjs.org/package/web-feeds-graphql)
[![Build Status](https://travis-ci.org/adieuadieu/web-feeds-graphql.svg?branch=master)](https://travis-ci.org/adieuadieu/web-feeds-graphql)
[![Coverage Status](https://coveralls.io/repos/github/adieuadieu/web-feeds-graphql/badge.svg?branch=master)](https://coveralls.io/github/adieuadieu/web-feeds-graphql?branch=master)

[![PeerDependencies](https://img.shields.io/david/peer/adieuadieu/web-feeds-graphql.svg?style=flat-square)](https://david-dm.org/adieuadieu/web-feeds-graphql#info=peerDependencies&view=list)
[![Dependencies](https://img.shields.io/david/adieuadieu/web-feeds-graphql.svg?style=flat-square)](https://david-dm.org/adieuadieu/web-feeds-graphql)
[![DevDependencies](https://img.shields.io/david/dev/adieuadieu/web-feeds-graphql.svg?style=flat-square)](https://david-dm.org/adieuadieu/web-feeds-graphql#info=devDependencies&view=list)

## Why?

tl;dr: XML is icky. JSON is neato. GraphQL is neato-ier.

Sometimes you're forced to reconsile the old with the new and here I've stumbled upon such a case that no one else has already solved for me :-(. Given that JSON is a thing, working with RSS/Atom is about as much fun as Myspace. But, when a client says, "Hey, I want you to display my friend Joe McBobberface's RSS feed on my spanking new GraphQL-backed app!" I roll my eyes and try to remember the last time I heard of/used/saw/thought about RSS (I dunno; maybe 5 years ago?) This project snowballed out of my attempt to reconsile said clients desire to display his friends RSS feed with trying to minimise the attack on the beauty of the app I've created for them.

## How

```
npm install web-feeds-graphql
```


```graphql
query {
  waitButWhy: feed(url: "http://waitbutwhy.com/feed") {
    channel {
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
}
```

feed object type
union of rss or atom

```js
import { RssObjectType } from 'web-feeds-graphql';



```


https://github.com/danmactough/node-feedparser

https://github.com/danmactough/node-feedparser/blob/master/examples/iconv.js


https://github.com/avajs/ava