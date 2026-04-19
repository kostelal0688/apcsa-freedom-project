# Entry 5(Finished MVP)
##### 4/15/26
## Content
Over the past week, I continued learning how to use SwiftUI to finish my Student Success App. I focused on improving how my app works and making sure all the main features are complete. I practiced using tools like @State and @Binding to update data, NavigationStack to move between screens, and Lists to display assignments. I also looked back at [tutorials](https://www.youtube.com/watch?v=xkgaIm7QxK0&list=PLMRqhzcHGw1ZHtM5xYcZbJ8oUZ0aVTasI) and [documentations](https://developer.apple.com/documentation/swiftui) and my previous code to fix mistakes and make everything run smoothly.

As I worked, I got better at understanding how different parts of SwiftUI connect. For example, I learned how to pass data between views so that when a user updates something, it changes everywhere in the app. This helped me make my app more interactive and user-friendly. [Here is a video of my MVP](https://drive.google.com/file/d/1J9DfwWUhtm8GL3jESqdmbnOhVSuk_OID/view).

### Finishing My MVP
This week, I completed my MVP. My app now allows users to:
* Add assignments with a title and due date
* View all assignments in a list
* Mark assignments as completed
* Navigate between the home screen and the tasks page
* Enter their name and an upcoming exam

These features meet my main goal, which is to help students stay organized and keep track of their schoolwork in one place.

One important part of finishing my MVP was making sure everything worked together. I tested adding assignments, checking them off, and moving between screens. I also made small improvements, like clearing the text fields after adding a task and organizing the layout so it looks cleaner.

Here is an example of how assignments are updated when completed:
```swift
assignments[realIndex].isDone.toggle()
```
This allows the app to instantly update when a user marks a task as done.

## Engineering Design Process 
Right now I am in Steps 5 and 6 of the engineering design process, which are building and testing the prototype. I built the main features of my app and tested them to make sure they work correctly. For example, I tested adding assignments, checking them off, and navigating between screens.

## Skills
Some skills that I’ve learned from working on this project are **Problem Solving** and **Debugging**

### Problem Solving
I used problem solving when figuring out how to connect different parts of my app. For example, I had to figure out how to pass the assignments list from one screen to another and update it correctly.

### Debugging
I used debugging when things did not work at first. For example, I fixed issues with updating assignments and making sure the correct task was marked as done. I checked my code and tested different solutions until it worked.

## Summary
Overall, I made strong progress toward my MVP by building the main features of my Student Success App. Users can now add assignments, view them, and mark them as complete. My next step is to improve the design and add more features, like editing assignments or adding reminders, to make the app even more useful.

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
