---
title: "Testing Closures Using Swift Testing"
date: 2024-11-03
tags: [swift, testing, ios]
---

if someone is looking to test closures using Swift Testing

```swift
@Test func handleURLMetadata() async throws {
        let url = try #require(URL(string: "https://www.doordash.com/backendYetToDecide"))
        await withCheckedContinuation { continuation in
            consumerRouter.presentUsingCompletionClosure = { routableType, routableStyle, _ in
                #expect(...)
                continuation.resume()
            }
            linkHandler.handle(url)
        }
    }
```
