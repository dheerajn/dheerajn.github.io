---
title: "String Comparison Performance in Swift"
date: 2024-09-29
tags: [swift, performance, ios]
---

When comparing two strings, it is always a good idea to search with String's built-in method rather than directly comparing .lowercased() becauseThe method .lowercased() creates a new copy of each String every time it's called, which might have a negative impact on performances.To provide a great user experience, you actually need more than just a case insensitive search!

```swift
let searchQuery = "jalapeno"
let searchQueryWithAccent = "jalapeño"

let comparisonResult = searchQuery.compare(searchQueryWithAccent, options: [.caseInsensitive, .diacriticInsensitive])

if comparisonResult == .orderedSame {
    print("both are equal")
}
```
