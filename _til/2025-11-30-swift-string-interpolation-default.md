---
title: "Swift 6.2 String Interpolation Default Value"
date: 2025-11-30
tags: [swift, ios]
---

In Swift 6.2, String interpolation has a new default value parameter that accepts a string regardless of the type of the optional value:

```swift
Text("The count is \(count, default: "not set")")
```
