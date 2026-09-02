---
name: gstack-design-review
description: >
  Visual / product-chrome audit against design-ui anti-slop. Use for "design
  review", "this looks generic", "polish the UI", "taste pass".
metadata:
  short-description: "Design review: tokens, slop, hierarchy"
user-invocable: true
---

# Design review

Open `design-ui` and its refined-ui reference. Then look at the running UI,
not the JSX in isolation.

Flag: extra hues, identical nested radii, emoji, marketing fluff, unreadable
muted text, tap targets under 44px, motion that fights reduced-motion.

Fix the system (tokens) before the one-off. Screenshot after.
