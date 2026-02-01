---
title: "iOS 26+ safeAreaBar"
description: "iOS 26+ introduces safeAreaBar modifier to show custom content as a bar beside the safe area. Perfect for bottom toolbars and custom UI."
date: 2026-01-24
tags: [swift, ios, swiftui]
image: /assets/images/til/safearea-bar.png
---

that we now use safeAreaBar from iOS 26+ to show the specified content as a custom bar beside the modified view

```swift
struct SafeAreaBarTest: View {
    var body: some View {
        NavigationStack {
            List {
                ForEach(1...20, id: \.self) { index in
                    Text("\(index). Item")
                }
            }
            .safeAreaBar(edge: .bottom) {
                Text("Hello, This is Bottom Bar!")
                    .padding(.vertical, 15)
            }
            .scrollEdgeEffectStyle(.soft, for: .bottom)
            //.scrollEdgeEffectStyle(.hard, for: .bottom)
        }
    }
}
```

<img src="/assets/images/til/safearea-bar.png" alt="safeAreaBar demo" style="max-width: 600px; height: auto;">
