---
title: Haptics
description: Haptics API
pluginapi: HapticsPlugin
contributors:
  - mlynch
  - jcesarmobile
---

<plugin-platforms platforms="ios,android"></plugin-platforms>

# Haptics

The Haptics API provides physical feedback to the user through touch or vibration.

<!--DOCGEN_INDEX_START-->
<!--DOCGEN_INDEX_END-->

## Android Notes

To use vibration, you must add this permission to your `AndroidManifest.xml` file:

```xml
<uses-permission android:name="android.permission.VIBRATE" />
```

## Example

```typescript
import {
  Plugins,
  HapticsImpactStyle
} from '@capacitor/core';

const { Haptics } = Plugins;

export class HapticsExample {
  hapticsImpact(style = HapticsImpactStyle.Heavy) {
    Haptics.impact({
      style: style
    });
  }

  hapticsImpactMedium(style) {
    this.hapticsImpact(HapticsImpactStyle.Medium);
  }

  hapticsImpactLight(style) {
    this.hapticsImpact(HapticsImpactStyle.Light);
  }

  hapticsVibrate() {
    Haptics.vibrate();
  }

  hapticsSelectionStart() {
    Haptics.selectionStart();
  }

  hapticsSelectionChanged() {
    Haptics.selectionChanged();
  }

  hapticsSelectionEnd() {
    Haptics.selectionEnd();
  }
}
```

<!--DOCGEN_API_START-->
<!--DOCGEN_API_END-->