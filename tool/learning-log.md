# Tool Learning Log

## Tool: **Swift**

## Project: **Student Success App**

---
### 10/27/25 - 11/2/2025:
* Swift is a programming language created by Apple. It’s used to make apps for iPhone, iPad, Mac, Apple Watch, and Apple TV.
    * **Safe and Fast:** Swift is designed to catch mistakes early and run apps quickly.
    * **Easy to Read**: Its code looks cleaner and simpler than older Apple languages like Objective-C.
    * **Modern Features:** Swift has tools like “optionals,” “type inference,” and “closures” that make coding easier and less error-prone.
    * **Used With SwiftUI:** Swift works with SwiftUI, a framework to build app interfaces visually, like buttons, lists, and forms.
Example of Swift Code :
```swift
// Print a greeting
let name = "Kostela"
print("Hello, \(name)!")
```
   * `let` creates a constant (a value that doesn’t change)
   * `print()` shows text on the screen
   * `\(name)` inserts the value of name into the message
* **Videos Watched**
   * [SwiftUI Tutorial for Beginners – Lists & Data](https://www.youtube.com/watch?v=F2ojC6TNwws) - Covers displaying multiple items, dynamic lists, and binding data with @State.
   * [SwiftUI Fundamentals Full Course](https://www.youtube.com/watch?v=b1oC7sLIgpI) - Beginner-friendly full course, including UI elements and state management.
* **Documentation & Guides:**
* [Apple SwiftUI List Documentation](https://developer.apple.com/documentation/swiftui/list) – Shows how to create lists, sections, and manage dynamic data.
* [Swift.org Basics](https://www.swift.org/getting-started/) – Simple guide for absolute beginners to understand Swift syntax and variables.
* [W3Schools Swift Tutorial](https://www.w3schools.com/swift/) - Very simple beginner-focused guide to Swift syntax and examples.
* [Swift Cheat Sheet](https://learnxinyminutes.com/swift/) – Quick reference for Swift syntax and commands for beginners.
* **Next Steps:**
  * Try making a small project to practice everything I’ve learned.

### 11/9/25 - 11/16/25
* [How to use NavigationStack in SwiftUI | Bootcamp #62](https://www.youtube.com/watch?v=GZ-hQWMjT0s) - covers creating a `NavigationStack`, using `NavigationDestination`, and handling navigation paths.
    * Learned the difference between `NavigationLink` and the newer `NavigationDestination`.
    * Understood how `NavigationStack` replaces NavigationView for better control.
    * Saw how navigation paths work when passing data between screens.
    * Realized that the new system is cleaner and more flexible for apps with multiple pages.
* [How to use NavigationStack in SwiftUI? (Deep Dive)](https://www.youtube.com/watch?v=fBbw6-Nu_lg)
    * Practiced sending custom data (like structs) to a new view through a navigation link.
    * Understood why `NavigationDestination` is important when you have more than one data type.
    * Saw how programmatic navigation works using a path array.
    * Understood common errors with `Hashable` and why SwiftUI needs it for navigation.
* [Complete Guide to Navigation in SwiftUI with NavigationStack (Article)](https://dev.to/yossabourne/complete-guide-to-navigation-in-swiftui-with-navigationstack-3npn)
    * Got a step-by-step breakdown of how a navigation stack works.
    * Learned how to create dynamic navigation where the destination depends on a data model.
    * Understood that `NavigationStack` is more scalable for real apps with many screens.
    * Helped clarify when to use `NavigationDestination` vs. just pushing a view normally.
<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
