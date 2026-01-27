---
title: "Parallax Effect in iOS 17"
date: 2024-12-27
tags: [swiftui, ios]
---

We can easily get the parallax effect from iOS 17 with just a few lines of code

```swift
VStack {
                        ZStack {
                            Image(imageName)
                                .resizable()
                                .scaledToFill()
                                .scrollTransition(axis: .horizontal) { content, phase in
                                    content
                                        .offset(x: phase.isIdentity ? 0 : phase.value * -250)
                                }
                        }
                        .containerRelativeFrame(.horizontal)
                        .clipShape(RoundedRectangle(cornerRadius: 36))
                    }
```
