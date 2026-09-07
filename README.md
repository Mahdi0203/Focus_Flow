# FocusFlow

FocusFlow is a lightweight desktop task planner built with **Java Swing**. It pairs an interactive monthly calendar with a simple to-do list, letting you navigate between months, select a day, and manage tasks in a clean, color-coded interface.

## Features

- **Interactive Calendar** — Browse months with previous/next navigation and click any date to select it.
- **Task Management** — Add tasks (up to 20 characters), view them in a scrollable list, and mark them complete with a single click.
- **Clean UI** — A custom teal/green color scheme with styled day labels and task cards.
- **Simple Interactions** — Pure mouse/keyboard driven Swing UI with no external dependencies.

## Tech Stack

- **Language:** Java
- **UI Framework:** Java Swing (AWT/Swing)
- **Date Handling:** `java.time` (LocalDate, YearMonth)

## Project Structure

```
Focus_Flow-main/
├── src/
│   └── FocusFlow/
│       ├── FocusFlow.java     # Application entry point
│       ├── Calendar.java      # Monthly calendar view & navigation
│       ├── DayLabel.java      # Custom JLabel for calendar day cells
│       ├── AddEvent.java      # Task input panel and task list
│       └── Event.java         # Task model + rendered task card
├── image/
│   ├── left.png               # Previous-month icon
│   └── right.png              # Next-month icon
└── bin/                        # Compiled .class files
```

## Getting Started

### Prerequisites

- Java Development Kit (JDK) 8 or later

### Running from the command line

```bash
# Clone the repository
git clone https://github.com/<your-username>/Focus_Flow.git
cd Focus_Flow

# Compile the source files
javac -d bin src/FocusFlow/*.java

# Run the application (from the project root, so image paths resolve)
java -cp bin FocusFlow.FocusFlow
```

### Running from an IDE (Eclipse/IntelliJ)

1. Import the project as a Java project.
2. Ensure `src` is marked as the source folder.
3. Set the working directory to the project root (so `image/left.png` and `image/right.png` resolve correctly).
4. Run `FocusFlow.java`.

## Usage

1. Launch the app — it opens on the current month with today's date highlighted.
2. Use the left/right arrow icons to move between months.
3. Click any date to select it.
4. Type a task into the text field and click **Add Task** to add it to your list.
5. Click the checkbox button next to a task to mark it as done.

## Roadmap / Ideas for Improvement

- [ ] Persist tasks to a file or database so they survive restarts
- [ ] Associate tasks with the specific selected date instead of a single global list
- [ ] Allow editing and deleting tasks
- [ ] Add due dates, reminders, and priority levels
- [ ] Package as a runnable JAR

## Author

Built as a personal Java Swing project to practice GUI development, event handling, and date/time APIs.
