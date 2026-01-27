---
title: "@frozen Attribute in Swift"
date: 2025-01-03
tags: [swift, performance]
---

The @frozen attribute in Swift indicates that a struct or enum's layout is fixed and won't change in future versions of the library or module where it is defined. This allows the compiler to make optimizations based on the assumption that the type won't gain new stored properties (for structs) or new cases (for enums) in the future.Faster Code: The compiler knows the fixed type, so it can optimize better.Simpler Code: No need to handle "future" cases in enums when using a switch.

```swift
@frozen public enum APIResult {
    case success
    case failure
}

// No need for `@unknown default` because the enum is frozen.
switch result {
case .success:
    print("Success")
case .failure:
    print("Failure")
}
```
