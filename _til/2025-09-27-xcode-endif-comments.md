---
title: "Xcode 26 #endif Comments"
date: 2025-09-27
tags: [xcode, ios, productivity]
---

Xcode 26 now shows the matching #if condition next to #endif. No more guessing or writing manual comments

```swift
#if DEBUG
    print("Debug mode")
#endif  // Xcode now automatically shows: #if DEBUG
```
