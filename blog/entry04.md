# Entry 4(Working toward  MVP)
##### 3/15/26

## Content
Over the past week, I have been learning how to build a calendar system in Swift for my Student Success App. My goal is for the app to help students organize assignments, study sessions, and goals by date. Instead of only showing a list of tasks, the calendar will allow students to visually see when their work is due and what they should focus on each day.

To learn how to build this feature, I watched several Swift tutorials and read documentation about calendar views. Some of the resources I used include [Monthly Calendar View App SwiftUI Xcode Tutorial](https://www.youtube.com/watch?v=jBvkFKhnYLI), [Custom Calendar Tutorial | SwiftUI](https://www.youtube.com/watch?v=nXdM4WMNDkg&t=176s), and [Calendar View in SwiftUI with MultiDatePicker](https://sarunw.com/posts/swiftui-multidatepicker/). These tutorials helped me understand how to build a calendar-style layout, create a month grid, allow users to select dates, and isplay events for specific days.

#### Progress Made
This week I started implementing the calendar and event structure for the app. I created a model called StudyEvent that stores information about a task or assignment. Each event has a title, subject, and date, which allows the app to organize tasks by the day they are due. I also added a graphical DatePicker that displays a calendar interface. When the user selects a date, the app filters the events and shows only the tasks scheduled for that day.

Here is part of the code I used to build this feature:
```swift
struct StudyEvent: Identifiable {
    let id = UUID()
    let title: String
    let subject: String
    let date: Date
}

This model stores the information for each study task.

Next, I added the calendar interface and connected it to the selected date.

@State private var selectedDate = Date()

DatePicker(
    "Select Date",
    selection: $selectedDate,
    displayedComponents: [.date]
)
.datePickerStyle(.graphical)
.padding()
```
The graphical date picker displays a calendar-style view, allowing the user to choose a specific day.

Then I created a system to filter events based on the selected date:
```
var filteredEvents: [StudyEvent] {
    events.filter { Calendar.current.isDate($0.date, inSameDayAs: selectedDate) }
}

This code checks whether each event occurs on the selected day and only displays those events.

Finally, I used a List to show the events for that date:

List(filteredEvents) { event in
    VStack(alignment: .leading) {
        Text(event.title)
            .font(.headline)
        Text(event.subject)
            .font(.subheadline)
    }
}
```
If there are no tasks scheduled, the app shows a message saying "No tasks for this day."
#### What I Learned
One important thing I learned is how SwiftUI updates the interface automatically when the selected date changes. By using @State, the list of events updates as soon as the user selects a different date on the calendar. I also learned how the Calendar function can compare dates to see if two events happen on the same day. Understanding how to filter data like this is important for organizing tasks in the app.
## Engineering Design Process
Right now I am working in Steps 5 and 6 of the engineering design process, which involve building and testing the prototype. I am building the prototype of the calendar system and testing how it works when users select different dates. My main goal right now is making sure the calendar correctly shows events for the selected day. Once the calendar works smoothly, I plan to add a feature that lets students add their own assignments and study tasks to the calendar.
## Skills
Some skills that I’ve learned from working on this project are **Problem Solving** and **Debugging**

### Problem Solving 
While working on the calendar feature, I had to figure out how to organize events by date and display them properly. I researched how SwiftUI handles dates and calendars, and I used that information to build a system that filters events for the selected day.

### Debugging
Debugging helped me when my events were not appearing correctly at first. I realized I needed to compare the dates using Calendar.current.isDate instead of checking the raw date values. After fixing that, the events started appearing correctly when the user selected a date.

## Summary
Overall, I made progress toward my MVP by creating a calendar interface that shows study events for specific days. This will help students see their assignments and study plans more clearly. My next step is to allow users to add their own events to the calendar, which will make the app more useful for managing school work.

[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
