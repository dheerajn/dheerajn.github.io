---
title: "SwiftUI RenameButton"
date: 2026-04-05
tags: [swift, ios, swiftui]
---

SwiftUI has a built-in RenameButton that you can use like this:

```swift
HStack {
    Text("Dheeru N")
    Spacer()
    RenameButton()
        .renameAction {
            // perform click operation
        }
}
```
