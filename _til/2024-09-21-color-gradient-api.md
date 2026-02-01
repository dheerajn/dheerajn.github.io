---
title: "iOS 16 Color Gradient API"
description: "iOS 16 added .gradient property to Color that returns a standard gradient. Easy way to add depth to text and shapes."
date: 2024-09-21
tags: [swiftui, ios]
image: /assets/images/til/color-gradient-api.png
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
