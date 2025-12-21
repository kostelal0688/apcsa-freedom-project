# Entry 2 (Learning My Tool)
##### 12/15/25

## Content
Over the past two weeks, I’ve been diving deeper into Swift and SwiftUI while working on a small Student Success App. My goal was to understand Swift fundamentals, SwiftUI state management, and how to structure a real app with multiple screens. Below, I’ll break down what I learned, including code examples, explanations, and challenges.

I started by reviewing beginner-friendly guides like [Apple’s step‑by‑step app building tutorials](https://docs.swift.org/swift-book/documentation/the-swift-programming-language/guidedtour/) and [Swift for Complete Beginners](https://www.hackingwithswift.com/quick-start/beginners) and practicing small coding exercises. Each day, I focused on one topic at a time:
* Swift Basics – Variables, constants, strings, numbers, Booleans, and arrays.
* Control Flow – `if/else statements`, for and while loops.
* Functions & Structs – Writing reusable functions and creating custom data types.
* SwiftUI Concepts – `@State`, `@Binding`, `NavigationStack`, and building simple views.
  
**Swift Basics**
* I started with the fundamentals of Swift, covering variables, constants, data types, control flow, functions, arrays, and structs.
  
**Variables, Constants & Data Types**
```swift
var greeting = "Hello, world!"     // a variable — value can change
let pi = 3.14159                   // a constant — value can’t change

print(greeting)  
print("Pi is \(pi)")               // string interpolation
```
* `var` declares a variable that can change.
* `let` declares a constant that cannot change.
* `print()` outputs to the console.
* `"\(pi)"` inserts the value of pi into a string.

**Conditional Statements & Loops**
```swift
let number = 7

if number % 2 == 0 {
    print("Even")
} else {
    print("Odd")
}

for i in 1...5 {
    print("i = \(i)")
}

var count = 1
while count <= 3 {
    print("count = \(count)")
    count += 1
}
```
* These exercises taught me how to control the flow of a program and repeat actions efficiently.

**SwiftUI Data Model**
```swift
struct Student: Identifiable, Hashable {
    let id = UUID()
    let name: String
    let grade: Int
    let gpa: Double
}
let student1 = Student(name: "Alice", grade: 11, gpa: 3.8)
let student2 = Student(name: "Bob", grade: 12, gpa: 3.5)
```
* Creating data models helped me organize real-world data (like student info) for use in my app.

### Winter Break Goal

## Engineering Design Process 

## Skills
Some skills that I’ve learned

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
