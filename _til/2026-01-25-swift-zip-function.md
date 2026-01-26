---
title: "Swift's zip() Function"
date: 2026-01-25
tags: [swift, ios]
---

Swift provides a solution with a built-in function called zip. This function allows for combining two sequences into a sequence of tuples, enhancing code cleanliness and readability.

```swift
import Foundation

let names = ["John", "Harry", "Brook"]
let scores = [72, 92, 78]

let pairedData = zip(names, scores)
for (name, score) in pairedData {
    print("\(name) scored \(score) points")
}
```

**Output:**
```
John scored 72 points
Harry scored 92 points
Brook scored 78 points
```
