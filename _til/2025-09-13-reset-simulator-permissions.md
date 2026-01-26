---
title: "Reset iOS Simulator Permissions"
date: 2025-09-13
tags: [ios, xcode, testing]
---

you can reset iOS Simulator permissions for your app without erasing the whole simulator

```bash
xcrun simctl privacy booted reset all <com.your.bundle.id>
```

This clears things like Contacts, Location, Camera, Photos, etc., so the next time your app asks, you'll see the system permission prompt again.

Super handy for testing different permission flows
