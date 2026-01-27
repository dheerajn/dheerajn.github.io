---
title: "Localized String Comparison in Swift"
date: 2024-12-15
tags: [swift, ios, localization]
---

When comparing strings that can vary by language or locale (e.g., backend-provided titles and locally stored titles in different languages), you can use String.compare(_:options:range:locale:) to handle case and diacritic insensitivity while respecting the system's locale settings. More hereUse .diacriticInsensitive to ignore accents (e.g., "é" == "e").Use .caseInsensitive to ignore case differences (e.g., "Apple" == "apple").Use Locale.current to adapt to the device's language settings dynamically.

```swift
import Foundation

func isLocalizedTitleEqual(backendTitle: String, localTitle: String) -> Bool {
    let comparisonResult = backendTitle.compare(localTitle, options: [.diacriticInsensitive, .caseInsensitive], range: nil, locale: Locale.current)
    return comparisonResult == .orderedSame
}

// Example usage
let backendTitle = "manzana" // Spanish for "apple"
let localTitle = "Manzana"  // Localized title

if isLocalizedTitleEqual(backendTitle: backendTitle, localTitle: localTitle) {
    print("The titles match!")
} else {
    print("The titles do not match.")
}
```
