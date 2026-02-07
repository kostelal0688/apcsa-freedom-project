# Entry 3
##### 2/7/26
## Content
Over winter break, I continued learning Swift and SwiftUI, focusing on how navigation works inside a real app. While I didn’t fully complete my original goal of building the entire Student Success App, I made meaningful progress by learning and practicing NavigationStack, NavigationLink, and list-based navigation. These concepts are essential for creating multi-screen apps, and they helped me better understand how users move through an app.

Instead of rushing to build the full app, I took time to focus on one important concept at a time: navigation in SwiftUI. I followed a step-by-step simple tutorial [How to use NavigationStack in SwiftUI](https://tnvmadhav.me/guides/how-to-use-navigationstack-in-swiftui/) that showed a basic NavigationLink opening another view, which helped me understand how screens connect. I also read [SwiftUI Navigation Concepts with code examples](https://www.codecademy.com/resources/docs/swiftui/navigation) to get a deeper explanation of NavigationStack and NavigationLink in different scenarios. To practice building lists that navigate to detail screens, I used [this guide on creating a list and navigation in SwiftUI](https://medium.com/swift-productions/create-a-list-with-navigation-swiftui-825bad03c940). I also watched a beginner YouTube video called [How to use NavigationStack in SwiftUI (YouTube)](https://www.youtube.com/watch?v=fBbw6-Nu_lg) explaining NavigationStack, which helped reinforce what I learned through reading and coding.

**Simple NavigationStack with a Button**
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
* `NavigationStack` creates the navigation environment.
* `NavigationLink` acts like a button that opens a new screen.
* The destination is the view that appears when the link is tapped.
* This showed me how apps can move from one screen to another instead of displaying everything on one page.
  
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
* A List displays multiple items.
* Each item has its own `NavigationLink`.
* Tapping an item opens a detail screen specific to that item.
* This is similar to how my app could show a list of students and then navigate to a detailed view with grades and GPA.


[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
