---
title: "Log Memory Usage Without Xcode"
date: 2025-10-05
tags: [swift, ios, debugging]
---

to log memory usage without Xcode

```swift
import Foundation

func snapshotMemoryUsage() -> Double {
    var taskInfo = task_vm_info_data_t()
    var count = mach_msg_type_number_t(MemoryLayout<task_vm_info>.size) / 4
    let result: kern_return_t = withUnsafeMutablePointer(to: &taskInfo) {
        $0.withMemoryRebound(to: integer_t.self, capacity: 1) {
            task_info(mach_task_self_,
                     task_flavor_t(TASK_VM_INFO),
                     $0,
                     &count)
        }
    }

    let usedMB = Double(taskInfo.phys_footprint) / Double(1024 * 1024)
    return result == KERN_SUCCESS ? usedMB : 0
}

print("Memory usage: \(String(format: "%.2f MB", snapshotMemoryUsage()))")
```

![Memory usage logging screenshot](/assets/images/til/memory-usage-logging.png)
