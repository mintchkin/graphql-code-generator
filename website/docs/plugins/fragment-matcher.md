---
id: fragment-matcher
title: Fragment Matcher
---

{@import ../generated-config/fragment-matcher.md}

## How to use?

## Usage with Apollo Client 3

If you are using Apollo Client 3, you need to specify the `apolloClientVersion: 3` configuration, and then use it in your Apollo cache instance:

```typescript
import { InMemoryCache } from '@apollo/client';

// generated by Fragment Matcher plugin
import { possibleTypes } from '../introspection-result';

const cache = new InMemoryCache({ possibleTypes });
```

> [Read more about fragment matcher and its usage on Apollo Client](https://www.apollographql.com/docs/react/data/fragments/#defining-possibletypes-manually)


## Usage with Apollo Client 2

```typescript
import { InMemoryCache, IntrospectionFragmentMatcher } from 'apollo-cache-inmemory';

// generated by Fragment Matcher plugin
import introspectionResult from '../introspection-result';

const fragmentMatcher = new IntrospectionFragmentMatcher({
  introspectionQueryResultData: introspectionResult,
});

const cache = new InMemoryCache({
  fragmentMatcher,
});
```
