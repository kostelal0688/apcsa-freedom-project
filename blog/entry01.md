# Entry 1 (Choosing a Tool and Topic)
##### 11/3/25

## Choosing a Tool & Topic
For my year-long project, I’ve chosen to create an app called Student Success using Swift. This app will help students stay organized, motivated, and supported throughout the school year. The goal is to make it easier for students to track their assignments, goals, and progress while also giving them access to helpful tips and resources that encourage good study habits, time management, and personal growth. I want the app to feel like a digital planner, study coach, and motivational tool all in one place, designed specifically for students who want to stay on top of their responsibilities.

The tool I’ve chosen to use for this project is Swift, Apple’s programming language for building iOS apps. Swift is known for being fast, safe, modern, and beginner-friendly, which makes it a great choice for developing mobile applications. It also integrates well with Xcode, Apple’s app development environment, which provides features like a user interface designer, live previews, templates, and debugging tools that make building apps much smoother and more visual. This helps me test ideas quickly and see how the app looks and behaves in real time.

I decided on Swift because I want to focus on creating a polished iOS app that students can easily access on their iPhones or iPads. Swift will allow me to design a clean, simple interface and include interactive features such as reminders, progress charts, study tips, scheduling tools, and goal tracking pages. I also plan to include notifications that remind students about deadlines and motivational messages that help them stay focused during busy weeks. Since Swift works well with frameworks like SwiftUI, I can also build smooth animations and organized layouts, which will make the app more enjoyable and easier to use.

. To learn more about Swift, I watched tutorials like [Learn Swift in 1 Hour](https://www.youtube.com/watch?v=FcsY1YPBwzQ). I also used [W3Schools Swift Guide](https://www.w3schools.io/languages/swift-tutorials/) to review syntax, experiment with small coding exercises, and understand core concepts such as variables, functions, structs, and objects. These resources helped me build a strong foundation in Swift and gave me confidence to start working on my project. Moving forward, I plan to explore more advanced lessons, such as working with NavigationStack, data models, and saving user information using UserDefaults or local storage. All of this learning will help me build a functional and well-designed Student Success app that supports students throughout the school year.

To start learning Swift, I tinkered with basic code to try simple SwiftUI projects. For example:
```swift
    // Testing variables and printing
    let name = "Kostela"
    print("Hello, \(name)!")
    
    // Practicing Swift models
    struct Task: Identifiable {
        let id = UUID()
        let title: String
    }
    
    let sample = Task(title: "Finish Homework")
    print(sample.title)
```
This helped me understand variables, printing, structs, UUIDs, and how data will work inside my app.
I also practiced SwiftUI by making a simple list:
```swift
    struct ContentView: View {
        @State private var tasks = ["Homework", "Study", "Project"]
    
        var body: some View {
            NavigationStack {
                List(tasks, id: \.self) { task in
                    Text(task)
                }
                .navigationTitle("Student Success")
            }
        }
    }
```
## Engineering Design Process 
I am currently in steps 1 and 2 of the engineering design process, which focus on defining and researching. First, I defined my topic by deciding to create an app that supports student success. Then, I researched the best tools and programming languages for building mobile apps. After comparing different options, I chose Swift because it allows me to design and develop an iOS app efficiently while learning real-world programming skills.

## Skills 
While working on my Student Success app, I’ve developed several important skills, including **Consideration** and **How to Google**
### Consideration
I learned to think carefully when choosing a tool for my project. I compared different programming languages and apps, like JavaScript, Python, and Swift, and considered which one would be best for building my Student Success app. I thought about what features I needed, how easy the tool would be to use, and how it would help my app work well for students.
### How to Google 
I practiced finding helpful tutorials, guides, and examples for Swift. I learned how to use the right search words, filter results to find the most useful sources, and focus on reliable websites. This helped me save time and find exactly what I needed to plan and start building my app.
## Summary
To conclude, I’m really excited to continue working on the Swift Student Success app. My next step will be to plan the app’s layout and start building the main features, such as the task list and goal tracker. I look forward to learning more about Swift and creating an app that can truly help students stay focused, motivated, and successful.

[Next](entry02.md)

[Home](../README.md)
