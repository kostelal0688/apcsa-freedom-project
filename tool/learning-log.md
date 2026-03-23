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
* This code creates a data model called Item. A model is just a blueprint for the kind of data your app uses.
 ```swift
   struct Item: Identifiable, Hashable {
       let id = UUID()
       let name: String
   }
```
`struct Item`
   * A struct is a container for data.
   * Here, it defines an “Item” object (like a fruit, task, or product).

`: Identifiable`
This tells SwiftUI that every Item has a unique id.
SwiftUI needs this to:
   * loop through lists
   * create navigation links
   * track which item belongs to which screen
Without Identifiable, List and NavigationStack won’t work smoothly.

`: Hashable`
   * This allows Swift to store the item in a Navigation path.
   * NavigationStack requires the data you push onto the stack to be Hashable, because it has to compare items, track history, and remove them cleanly.
   * If your model isn’t Hashable → errors in NavigationStack.

`let id = UUID()`
   * Creates a unique number (like a digital fingerprint) for each item.
   * Every Item gets its own random UUID.
   * This helps SwiftUI tell items apart even if two items have the same name.
Example:
   * Two items both named “Apple” would still have different IDs.

`let name: String`
   * Stores the name of the item (like “Apple”, “Banana”, etc.).
   * You decide what the name is when creating the item.

### 11/17/25 - 11/23/25
* [SwiftUI ForEach Documentation](https://www.hackingwithswift.com/quick-start) – Helped reinforce how to use bindings, state, and environment objects.
```swift
struct Product: Identifiable, Hashable {
    let id = UUID() 
    let title: String
    let price: Double
}
```
`struct Product`
* A struct is a container for data.
* Defines a “Product” object with a title and price.
`: Identifiable`
* Ensures each product has a unique ID.
* Needed for lists and navigation links in SwiftUI.
`: Hashable`
* Allows SwiftUI to store items in a NavigationStack.
* Ensures each item can be compared and tracked in the stack.
`let id = UUID()`
* Generates a unique identifier for every product.
* Even two products with the same title will be treated as unique.
`let title: String & let price: Double`
* Stores the name and cost of the product.
* Practiced using this data in dynamic lists and passing it between views.
  
### 12/1/2025 - 12/7/2025
* [Apple Docs – State & Data Flow](https://developer.apple.com/documentation/swiftui/model-data)
   * Official explanation of `@State`, `@Binding`, and `@ObservedObject`
   * How SwiftUI updates the UI automatically when data changes
* [Swift for Complete Beginners](https://www.hackingwithswift.com/quick-start/beginners)
   * This is a beginner-friendly guide to learning the basics of the Swift language.
   * Fundamental Swift syntax & data types — The guide covers variables and constants, Strings, numbers (integers and decimals), Booleans, and basics of how to store and use data. 
   * Control flow, collections, and data structures — You learn about conditions (if, switch), loops (for, while), and complex data structures such as arrays, dictionaries, and sets.
   * Functions, optionals, and closures — Teaches how to write reusable code (functions), handle optional (i.e. maybe-present) data safely, and manage functional programming features like closures.
   * Structs, classes, protocols, and more advanced features — The guide introduces Swift’s advanced tools: how to build your own types with struct or class, manage shared behaviors with protocols, extend types, and use other key features. 
#### Variables / Constants / Data Types
```swift
   var greeting = "Hello, world!"     // a variable — value can change
   let pi = 3.14159                  // a constant — value can’t change
   
   print(greeting)  
   print("Pi is \(pi)")             // string interpolation
```

* `var` declares a variable that can change.
* `let` declares a constant that cannot change.
* `print()` outputs to the console.
* `"\(pi)"` inserts the value of pi into a string.
#### Conditional statements and loops
```swift
   let number = 5
   
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

* `if … else` lets you choose code paths based on conditions.
* `for i in 1...5` loops `i` from 1 to 5.
* `while` repeats a block while a condition is true.
#### Functions
```swift
func greet(person name: String) -> String {
    return "Hello, \(name)!"
}

let message = greet(person: "Kostela")
print(message)    // prints: Hello, Kostela!
```

* `func` defines a function.
* `-> String` means the function returns a String.
* Functions let you reuse logic
####  Arrays & simple struct
```swift
var fruits = ["Apple", "Banana", "Cherry"]
fruits.append("Date")
print(fruits)   // ["Apple", "Banana", "Cherry", "Date"]

struct Person {
    var name: String
    var age: Int
}

let someone = Person(name: "Alex", age: 20)
print("Name: \(someone.name), Age: \(someone.age)")
```
* Arrays hold ordered lists of values.
* `.append(...)` adds an item.
* `struct` is a way to bundle related data (like name and age).
* **Next Steps:**
  * Try to stat parts of mt project to practice everything I’ve learned.
### 12/8/2025 - 12/13/2025
* Continued developing skills in Swift and SwiftUI for my Student Success App.
* Focused on understanding how app structure works in real projects, especially how data, navigation, and views connect.
* Spent time reviewing past notes and examples to reinforce key concepts instead of rushing ahead.
* Started thinking about how this app could realistically help students stay organized and track progress.
#### Concepts Deepened
* **NavigationStack**
* Learned how multiple screens can be stacked and navigated smoothly.
* Better understood how SwiftUI keeps track of where the user is in the app.
* **Data Models**
* Practiced creating models that represent real users and information.
* Learned why clean data models make apps easier to expand later.
* **State & Data Flow**
* Improved understanding of how SwiftUI updates the interface automatically when data changes.
* Learned why managing state correctly prevents bugs and confusing behavior.
* **Practice Code**
```swift
struct Student: Identifiable, Hashable {
    let id = UUID()
    let name: String
    let grade: Int
    let gpa: Double
}
```
* Expanded the Student model to include GPA.
* This model could be used to track academic progress inside the app.
* Learned how adding properties affects how data is displayed and passed between views.

**What I Learned**
* SwiftUI relies heavily on data-driven design.
* Navigation feels simpler once the data model is set up correctly.
* Small mistakes in state management can cause large issues in navigation.
  
**Challenges**
* Passing data cleanly between views still feels confusing at times.
* Remembering when to use @State vs. @Binding requires more practice.
* Debugging logic errors takes patience, especially when the UI doesn’t update as expected.

  
**Next Steps**
* Build a basic dashboard screen for the Student Success App.
* Add sample student data and display it in a List.
* Practice passing selected student data to a detail view.
* Continue reviewing SwiftUI state and navigation concepts.

### 1/12/2026 - 1/15/2026
* [How to use NavigationStack in SwiftUI(simple tutorial)](https://tnvmadhav.me/guides/how-to-use-navigationstack-in-swiftui/) - shows a basic NavigationStack with a NavigationLink that opens another view.
* [SwiftUI Navigation Concepts (with code examples)](https://www.codecademy.com/resources/docs/swiftui/navigation) - explains NavigationStack and NavigationLink in detail.
* [Create a list and navigation in SwiftUI](https://medium.com/swift-productions/create-a-list-with-navigation-swiftui-825bad03c940) - shows how to build a list that can navigate to detail screens.
* [How to use NavigationStack in SwiftUI (YouTube)](https://www.youtube.com/watch?v=fBbw6-Nu_lg) - beginner video explaining how NavigationStack works.

**Simple NavigationStack with a Button Link**
  ```swift
     import SwiftUI

      struct ContentView: View {
          var body: some View {
              NavigationStack {
                  NavigationLink("Go to Second Screen", destination: Text("Hello from the second screen"))
                      .navigationTitle("Home")
              }
          }
      }
  ```
- This code shows a basic screen with a button that opens a new screen when tapped.

**NavigationStack with a List**
  ```swift
     import SwiftUI

      struct ContentView: View {
          let items = ["Apples", "Bananas", "Cherries"]
      
          var body: some View {
              NavigationStack {
                  List(items, id: \.self) { item in
                      NavigationLink(item, destination: Text("Detail for \(item)"))
                  }
                  .navigationTitle("Fruits")
              }
          }
      }

  ```
- Here a list shows several items, and tapping any takes you to a detail view. This is useful for apps with lists of data
### 3/2/2026 - 3/8/2026
* This week I started planning how the Student Success App will work like a calendar. Instead of only showing lists of students or tasks, the app will allow users to see assignments, goals, or study tasks organized by date.
* A calendar structure could help students manage their time, track assignments, and plan study sessions more easily.
Watched these videos"
* [Monthly Calendar View App SwiftUI Xcode Tutorial](https://www.youtube.com/watch?v=jBvkFKhnYLI)
* [Custom Calendar Tutorial | SwiftUI](https://www.youtube.com/watch?v=nXdM4WMNDkg&t=176s)
* These tutorials show:
  * How to build a calendar layout
  * How to create a month grid
  * How users can tap dates to view events
* [Calendar view in SwiftUI with MultiDatePicker](https://sarunw.com/posts/swiftui-multidatepicker/) - This explains how SwiftUI can display a calendar-like date picker and allow users to select dates.
```swift
   import SwiftUI

struct StudyEvent: Identifiable {
    let id = UUID()
    let title: String
    let subject: String
    let date: Date
}

struct ContentView: View {

    @State private var selectedDate = Date()

    let events = [
        StudyEvent(title: "Math Homework", subject: "Math", date: Date()),
        StudyEvent(title: "Biology Quiz Study", subject: "Biology", date: Date()),
        StudyEvent(title: "History Essay", subject: "History", date: Date().addingTimeInterval(86400))
    ]

    var filteredEvents: [StudyEvent] {
        events.filter { Calendar.current.isDate($0.date, inSameDayAs: selectedDate) }
    }

    var body: some View {
        NavigationStack {
            VStack {

                // Calendar style date picker
                DatePicker(
                    "Select Date",
                    selection: $selectedDate,
                    displayedComponents: [.date]
                )
                .datePickerStyle(.graphical)
                .padding()

                // Events for selected day
                List(filteredEvents) { event in
                    VStack(alignment: .leading) {
                        Text(event.title)
                            .font(.headline)
                        Text(event.subject)
                            .font(.subheadline)
                    }
                }

                if filteredEvents.isEmpty {
                    Text("No tasks for this day")
                        .foregroundColor(.gray)
                        .padding()
                }
            }
            .navigationTitle("Study Calendar")
        }
    }
}
```
#### What This Code Does
- StudyEvent Model
    - Stores a task or assignment.
    - Includes a title, subject, and date.
- DatePicker (.graphical)
   - Displays a calendar-style interface.
   - Lets the user select a day.
- Filtering Events
```swift
events.filter { Calendar.current.isDate($0.date, inSameDayAs: selectedDate) }
```
   - Shows only events for the selected day.
- List
   - Displays tasks scheduled for that date.

### 3/16/2026 - 13/23/2026
This week I continued improving the calendar feature and started connecting it more directly to the overall purpose of the Student Success App. I focused on making the app feel more interactive and useful rather than just displaying information.

#### Concepts Worked On
* User Interaction
* Practiced making the app respond to user actions like selecting a date or tapping on an event.
* Improved understanding of how SwiftUI updates the screen when the user interacts with elements.
* Refining the Calendar Feature
* Worked on improving how events are displayed for each selected date.
* Considered adding features like marking tasks as completed or highlighting important dates.
* Continued practicing when to use @State for simple data and how it affects UI updates.
* Reinforced how changing the selected date automatically refreshes the event list.
* Experimented with adding more properties like priority or completion status.

#### Example idea:
```swift
struct StudyEvent: Identifiable {
    let id = UUID()
    let title: String
    let subject: String
    let date: Date
    var isCompleted: Bool
}
```
This allows the app to eventually:
* Track completed assignments
* Show progress over time
* Help students stay organized

#### What I Learned
* Small UI improvements can make the app feel much more useful.
* Thinking about real users helps guide better design decisions.
* [SwiftUI Learning Roadmap / Beginner Resources](https://www.swiftyplace.com/no-experience-to-first-ios-job-beginners?#1_Get_Familiar_with_Xcode)
#### Next Steps
* Add a way to mark tasks as completed.
* Continue improving the calendar UI and usability.
  
### 3/23/26
[Tutorial](https://www.youtube.com/watch?v=F2ojC6TNwws)
(https://www.swiftyplace.com/no-experience-to-first-ios-job-beginners?#1_Get_Familiar_with_Xcode)
<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still havea
* What you're going to try next
-->
