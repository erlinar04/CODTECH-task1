NAME:ERLINA R
COMPANY NAME:CODTECH IT SOLUTIONS PVT.LTD
ID:CT6WDS1833
DOMAIN:SOFTWARE DEVELOPMENT
DURATION:SEPTEMBER 15 TO OCTOBER 30
MENTOR:NEELA SANTHOSH KUMAR

OVERVIEW OF THE PROJECT:
### Overview of the To-Do List Android App

This simple Android To-Do List application allows users to create, view, and delete tasks, storing them locally on the device using SQLite, Android’s lightweight database. Below is a high-level breakdown of the project components, functionality, and flow.

### Project Structure

1. **`MainActivity.java`**:
   - Acts as the main activity that provides the user interface and handles the core logic.
   - Manages task input, addition, deletion, and displays tasks in a list.
   - Contains a nested SQLite helper class, `TaskDatabaseHelper`, which interacts with the database.

2. **`TaskDatabaseHelper` (Inner Class in `MainActivity.java`)**:
   - Handles SQLite database operations, including creating tables, adding tasks, fetching tasks, and deleting tasks.
   - Manages database upgrades as necessary, allowing the app to remain functional with new versions.

3. **Layout File (`activity_main.xml`)**:
   - Provides a simple, clean interface layout with an `EditText` input, a `Button` for adding tasks, and a `ListView` to display the list of tasks.
   - Uses basic UI elements to keep it lightweight and accessible.

### Key Functionalities

1. **Add Task**:
   - User enters a task description in the `EditText` field and clicks the "Add Task" button.
   - The app inserts the task into the SQLite database via `TaskDatabaseHelper` and updates the displayed list of tasks.

2. **Display Tasks**:
   - On app startup, `MainActivity` retrieves tasks from the database and populates the `ListView`.
   - Tasks are displayed in a simple list with each item represented by its description.

3. **Delete Task**:
   - Long-pressing a task in the list triggers a deletion.
   - The app removes the selected task from the SQLite database and updates the list in real-time.

### App Flow

1. **Startup**:
   - `MainActivity` is launched.
   - The app initializes the UI elements, sets up listeners, and loads tasks from the database.

2. **User Interactions**:
   - Users can add tasks, which are saved in the SQLite database and immediately appear in the `ListView`.
   - Users can long-press tasks to delete them, both visually and from the database.

3. **Database Persistence**:
   - Tasks are stored in a local SQLite database file (`tasks.db`), ensuring data persists even if the app is closed or the device is restarted.
   - The database is managed by `TaskDatabaseHelper`, which creates the table on the first run, and inserts, queries, or deletes records as needed.

### Technologies and Concepts Used

- **Java**: The primary programming language for Android app development.
- **SQLite**: A lightweight, relational database for storing data locally on the device.
- **Android UI Components**:
   - `EditText` for input.
   - `Button` for action triggers.
   - `ListView` for displaying tasks.
- **Event Handling**:
   - `OnClickListener` for handling button presses.
   - `OnItemLongClickListener` for handling task deletion via long-press on list items.

### Potential Enhancements

1. **Task Completion Status**: Add checkboxes to mark tasks as complete, or implement a swipe-to-complete feature.
2. **Edit Tasks**: Allow users to modify existing tasks.
3. **Data Backup**: Sync data to cloud storage, allowing for backups and access across devices.
4. **Custom Styling**: Improve the UI by adding custom icons, themes, and animations.

This project provides a foundation for developing more advanced to-do list features, such as reminders, prioritization, and categorization.
