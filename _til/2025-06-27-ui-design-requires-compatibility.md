---
title: "UIDesignRequiresCompatibility for Liquid Glass Design"
description: "Opt out of iOS Liquid Glass design with UIDesignRequiresCompatibility in Info.plist. Temporary solution until Xcode 27 removes it."
date: 2025-06-27
tags: [ios, xcode]
---

if you add UIDesignRequiresCompatibility to your Info.plist and set it to YES, your app will run using the old OS design instead of the new Liquid Glass design.
Apple will remove this starting Xcode 27 so we have a bit of time to migrate.
