# json-types

> JSON TypeScript Definitions
>
> A simple typescript definition module that simplifies type checking for valid JSON objects. Useful for defining interfaces and parameter type checking.

## Installation

```shell
npm i json-types
```

## Usage

```typescript
import {
  Primitive,
  JSONEntry,
  JSONArray,
  JSONMap,
  JSONData
} from '../json-types'
```

### Use Case

```typescript
import {
  Primitive,
  JSONEntry,
  JSONArray,
  JSONMap,
  JSONData
} from '../json-types'

interface QueryString {
  [key: string]: Primitive | undefined
}

interface APIResponse extends JSONMap {
  address: {
    house_no: number
    street: string
  }
  name: string,
  has_website: false
  files: JSONArray
  metadata: JSONEntry
}

function httpGet (url: string): Promise<JSONData> {
  return requestPromise(url, {
    json: true
  })
}
```
