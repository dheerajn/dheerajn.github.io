---
title: "iOS 26+ safeAreaBar"
date: 2026-01-24
tags: [swift, ios, swiftui]
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

![safeAreaBar demo](/assets/images/til/safearea-bar.png)
