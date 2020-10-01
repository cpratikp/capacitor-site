---
title: Browser
description: Browser API
contributors:
  - mlynch
  - jcesarmobile
---

<plugin-platforms platforms="pwa,ios,android"></plugin-platforms>

# Browser

<plugin-api-index name="browser"></plugin-api-index>

The Browser API makes it easy to open an in-app browser session to show external web content,
handle authentication flows, and more.

On iOS this uses `SFSafariViewController` and is compliant with leading oAuth service in-app-browser requirements.

```typescript
import { Plugins } from '@capacitor/core';

const { Browser } = Plugins;

await Browser.open({ url: 'http://capacitorjs.com/' });
```

## API

<plugin-api name="browser"></plugin-api>