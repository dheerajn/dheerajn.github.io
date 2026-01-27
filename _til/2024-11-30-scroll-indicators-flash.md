---
title: "Flash Scroll Indicators in SwiftUI"
date: 2024-11-30
tags: [swiftui, ios]
---

bout the scrollIndicatorsFlash modifier in SwiftUI (iOS 17+), which flashes the scroll indicators of scrollable views whenever a bound value changes. This is great for drawing attention to scrollable content, ensuring users don't miss important information. Learn more in the official Apple documentation.

```swift
ScrollView {
                VStack {
                    ForEach(0..<50, id: \.self) { index in
                        Text("Row \(index)")
                            .padding()
                    }
                }
            }
            .scrollIndicatorsFlash(trigger: flashScrollIndicators)

            Button("Flash Scroll Indicators") {
                flashScrollIndicators.toggle()
            }
            .padding()
```
