---
title: 'Understanding Deep Copy and Shallow Copy in Swift'
date: 2020-03-26
permalink: /posts/2020/03/deep-copy-shallow-copy-swift/
tags:
  - Swift
  - iOS
  - Programming
summary_points:
  - "Explains the difference between Swift value types and reference types."
  - "Compares deep copy and shallow copy behavior in real application code."
  - "Shows how `NSCopying` enables independent copies for class-based models."
---

*Originally published on [Medium](https://ankur098.medium.com/understanding-deep-copy-and-shallow-copy-in-swift-8df201375611) — March 26, 2020*

---

Swift organizes its types into two broad categories:

- **Value Type** — each instance holds its own independent copy of data (e.g. `struct`)
- **Reference Type** — instances share a single copy of data (e.g. `class`)

Understanding how copying works across these two categories is essential for writing safe, predictable Swift code.

## Deep Copy

A deep copy duplicates all data completely. Structures use this by default — every copy is fully independent. This makes deep copies safe in multi-threaded environments, though slightly slower due to the memory duplication involved.

## Shallow Copy

A shallow copy only duplicates the reference, not the underlying object. Classes use this approach by default. Multiple variables point to the same memory location, making copies fast but risky in concurrent scenarios where a change through one reference affects all others.

## Making Classes Support Deep Copy

Reference types can opt into deep copying by conforming to Apple's `NSCopying` protocol. Implementing the required `copy` method produces a genuinely independent object — even for classes — giving you the safety of a value type when you need it.

> *"Functional copies of themselves that are functionally independent objects with values identical to the original at the time the copy was made."* — Apple Documentation

## Practical Takeaway

While classes share references by default, `NSCopying` gives you the flexibility to create true independent copies when your design demands it.

---

Read the full article with code on [Medium →](https://ankur098.medium.com/understanding-deep-copy-and-shallow-copy-in-swift-8df201375611)
