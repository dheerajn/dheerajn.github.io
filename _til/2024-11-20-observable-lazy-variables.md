---
title: "Lazy Variables Not Supported with @Observable"
date: 2024-11-20
tags: [swift, swiftui, ios]
---

When migrating to @Observable, lazy variables are not supported. Replace them with computed properties or initialize them directly to ensure compatibility or use @ObservationIgnored

```swift
@Observable
class WalksViewModel {
    let walks = [
        Walk(title: "Central Park Loop", difficulty: .easy),
        Walk(title: "Mountain Ridge Trail", difficulty: .hard),
        Walk(title: "Riverbank Stroll", difficulty: .medium)
    ]

    var sortingIsOn = false

    @ObservationIgnored
    lazy var sortedWalks: [Walk] = {
        walks.sorted(
            using: KeyPathComparator(\Walk.difficulty)
        )
    }()
}
```
