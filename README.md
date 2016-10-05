# Web Feeds GraphQL
Reconsiling old shit with new shit; Query Web Feeds (RSS, Atom, and RDF) with GraphQL

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