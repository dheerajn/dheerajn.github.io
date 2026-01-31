---
title: "Reset iOS Simulator Privacy Permissions"
date: 2025-05-23
tags: [ios, xcode, simulator]
---

You can reset all privacy permissions (camera, location, contacts, etc.) on the iOS Simulator using this one-liner:

```bash
xcrun simctl privacy booted reset all
```

Perfect for testing first-time permission prompts or running UI tests in a clean state.

No need to reset the simulator or reinstall the app — just clear permissions and go.
