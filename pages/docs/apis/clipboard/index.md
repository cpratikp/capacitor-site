---
title: Clipboard
description: Clipboard API
contributors:
  - mlynch
  - jcesarmobile
---


<plugin-platforms platforms="pwa,ios,android"></plugin-platforms>

# Clipboard

The Clipboard API enables copy and pasting to/from the clipboard. On iOS this API also allows 
copying images and URLs.

<plugin-api-index name="clipboard"></plugin-api-index>

## Example

```typescript
import { Plugins } from '@capacitor/core';

const { Clipboard } = Plugins;

Clipboard.write({
  string: "Hello, Moto"
});

let result = await Clipboard.read();
console.log('Got', result.type, 'from clipboard:', result.value);
```

## API

<plugin-api name="clipboard"></plugin-api>