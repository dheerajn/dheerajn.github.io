---
title: "iOS 16 Color Gradient API"
date: 2024-09-21
tags: [swiftui, ios]
---

TIL: iOS 16 has an API that returns the standard gradient for the color self

```swift
HStack {
                Text("Some text")
                    .foregroundStyle(Color.purple)
                    .font(.largeTitle)

                Divider()

                Text("Some text")
                    .foregroundStyle(Color.purple.gradient)
                    .font(.largeTitle)
            }
```

![Color gradient comparison](/assets/images/til/color-gradient-api.png)
