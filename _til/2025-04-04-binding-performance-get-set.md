---
title: "SwiftUI Binding Performance: Keypath vs get/set"
description: "Use keypath bindings ($value) over Binding(get:set:) for better SwiftUI performance. Avoid unnecessary re-renders with efficient comparisons."
date: 2025-04-04
tags: [swift, swiftui]
---

Favor keypath-based bindings (like `$value`) over manually constructed bindings using `Binding(get:set:)` in production code.

Manual bindings create closures that SwiftUI cannot effectively compare, leading to unnecessary view re-renders. Keypath bindings allow SwiftUI to perform efficient field-by-field comparisons and skip unnecessary rendering updates.

[https://chris.eidhof.nl/post/binding-with-get-set/](https://chris.eidhof.nl/post/binding-with-get-set/)
