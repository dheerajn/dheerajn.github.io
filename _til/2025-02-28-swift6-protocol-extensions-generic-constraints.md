---
title: "Swift 6.0 Protocol Extensions with Generic Constraints"
date: 2025-02-28
tags: [swift]
---

In Swift 6.0, protocol extensions get enhanced support for generic constraints

```swift
protocol Serializable {
    func serialize() -> String
}

extension Serializable where Self: Encodable {
    func serialize() -> String {
        let encoder = JSONEncoder()
        guard let data = try? encoder.encode(self),
              let json = String(data: data, encoding: .utf8) else {
            return "{}"
        }
        return json
    }
}
```
