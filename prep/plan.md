# Plan

## Tool: Swift
## Product: Student Success App

---

## Timeline

#### MVP
  - [ ]  **Create Welcome Screen (2/15 - 2/18)**
     - [ ] Design a simple intro screen for the app
       - [ ] Add app title and short motivational tagline and a “Get Started” button to navigate to calendar
   - [ ] **Build Monthly Calendar View (2/19 - 2/22)**
       - [ ] Create monthly calendar layout
           - [ ] Add dots for days with tasks
              - [ ] Allow user to tap a day to open Daily Task View
   - [ ] **Create Daily Task View (2/23 - 2/25)**
        - [ ] Display list of tasks for selected day
            - [ ] Add checkbox toggle to mark tasks complete
                - [ ] Show empty state message if no tasks
                  - [ ] Add navigation back to monthly calendar        
  - [ ]  **Add Event / Assignment Screen (2/26 - 2/28)**
    - [ ]  Create form to input task details
      - [ ]  Add title text field, date picker, priority selector (Low / Medium / High), and save button to store event
  - [ ]  **Display Daily Motivational Quote (3/1 - 3/3)**
     - [ ]  Create array of motivational quotes
       - [ ]  Randomly select one quote per day
        - [ ]  Display quote at top of dashboard
  - [ ]  **Highlight Upcoming Deadlines (3/4 - 3/7)**
    - [ ]   Use conditional logic to detect tasks due within 24 hours
      - [ ]   Display “Due Soon” label
        - [ ]   Change task text color to red
   - [ ]  **Add Simple Progress Tracker (3/8 - 3/14)**
     - [ ]  Calculate percentage of completed tasks per day
        - [ ]  Display progress bar on dashboard
          - [ ]  Update progress dynamically when tasks are completed

#### Beyond MVP
- [ ] **Push notifications with motivational messages or basic reminder notification before due date**
  - [ ] Morning reminder message
- [ ] **Streak tracker (days productive in a row)**
  - [ ] Track consecutive days with completed tasks
    - [ ] Display streak number on dashboard
- [ ] **Customizable themes (light / dark mode toggle)**
  - [ ]  Allow user to choose accent color
- [ ] **Goal setting page**
  - [ ] User sets weekly productivity goal
    - [ ] Show progress toward goal





<!-- EXAMPLE

## Tool: APIs
## Product: Green Glass Door riddle app

## Timeline

### MVP

- [ ] Front-end
  - [x] Webpage to collect input from user (deadline: 4/15)
  - [ ] Webpage to display "yes, but a ___ can't" or "no, but a ___ can" (deadline: 5/1)
- [x] Back-end
  - [x] Use regex to test whether or not the word can go through the GGD (deadline: 3/1)
  - [x] Use the Twinword API to find related words (deadline: 3/15)
    - [ ] Iterate through the words until an opposite example can be found (deadline: 4/1)

#### Beyond MVP

- [ ] Use another API to make sure the opposite example is a noun
- [ ] Automate notification of API limit to make sure I don’t exceed free quota
- [ ] A multiple choice quizzer that will test the user’s knowledge of the solution

-->





<!-- DO NOT USE THIS YET

#### Peer Feedback 

| Name | Glows | Grows |
| -------- | ------- | ------- |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |
|  |  |  |

-->
