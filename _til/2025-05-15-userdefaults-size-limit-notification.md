---
title: "UserDefaults Size Limit Notification"
description: "Monitor UserDefaults size with UserDefaults.sizeLimitExceededNotification. Apple's built-in alert for when you exceed storage limits."
date: 2025-05-15
tags: [swift, ios, userdefaults]
---

UserDefaults has a size limit, and Apple provides a notification for when you go over it: [UserDefaults.sizeLimitExceededNotification](https://developer.apple.com/documentation/foundation/userdefaults/sizelimitexceedednotification)

It's posted by the system when your app stores more data in UserDefaults than the platform allows. If you're using UserDefaults for anything beyond small preferences (like large arrays or blobs), you're doing it wrong — and this notification can alert you before things silently break.

You can listen for it like this:

```swift
NotificationCenter.default.addObserver(
    forName: UserDefaults.sizeLimitExceededNotification,
    object: nil,
    queue: .main
) { _ in
    print("UserDefaults size limit exceeded!")
    // Consider logging or cleaning up large keys
}
```
