---
title: "Custom Spinner Messages in Claude Code"
date: 2026-04-04
tags: [claude, cli, tools]
---

I can now set up a new claude custom spinner/loading message like so

Add to ~/.claude/settings.json:

```json
"spinnerVerbs": {
    "mode": "replace",
    "verbs": [
        "Brewing coffee virtually",
        "Consulting the rubber duck",
        "Reticulating splines",
        "Warming up the flux capacitor",
        "Asking the magic 8-ball",
        "Counting backwards from infinity",
        "Untangling spaghetti code",
        "Negotiating with the compiler",
        "Feeding the hamsters",
        "Aligning the pixels",
        "Summoning the code gods",
        "Polishing the bits"
    ]
}
```
