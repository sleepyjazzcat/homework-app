📚 Academic Planner: Real-Time Task Manager
Overview
The Academic Planner is a modern, responsive web application designed to help students track assignments, projects, and exams in a clean, real-time interface. It utilizes Google Firestore to provide persistent, collaborative data storage across sessions and devices.

✨ Features
This planner is built around five core pages accessible via the navigation bar:

1. Dashboard (dashboard.html)

Summary Metrics: Shows the total number of upcoming tasks and the due date of the very next assignment.

Quick Access: Provides a feed of the top three assignments due soon.

Manual Entry: Features a prominent link to the Add New Assignment form.

2. Add New Assignment (add-assignments.html)

A dedicated, responsive form for manually inputting new assignments.

Allows users to specify the Assignment Title, Class, Due Date, Priority (High, Medium, Low), and a Description.

Submits data directly to the real-time Firestore database.

3. Assignments (assignments.html)

Comprehensive List: Displays all assignments, sortable by completion status (Upcoming vs. Completed).

Detail View: Clicking an assignment provides a detailed view showing all stored information.

Completion Tracking: Users can mark individual tasks as complete, instantly updating the dashboard and calendar.

4. Calendar View (index.html)

The application's homepage provides a visual, month-by-month calendar view.

Assignments are displayed as visual indicators on their respective due dates.

5. Settings (settings.html)

User Preferences: Includes a functional Dark Mode Toggle to switch between light and dark themes.

Data Management: Displays the unique User ID and provides an option to clear all synchronized assignment data from the database.

💻 Technology Stack
The Academic Planner is a single-file, client-side web application built using modern web standards:

HTML5: Application structure.

Tailwind CSS: Fully responsive, utility-first styling for a professional and modern look.

JavaScript (ES6+): Application logic, data handling, and state management.

Google Firebase/Firestore: Used for real-time, persistent, and collaborative data storage. Assignments are stored in a public collection so they can be viewed and updated by any authenticated user.

🔒 Data Persistence
This application uses Firestore for all assignment data.

Collection Path: /artifacts/{appId}/public/data/assignments

Authentication: The application initializes Firebase and authenticates the user upon load (using an anonymous token if no initial token is provided).

Real-time Updates: All views (Dashboard, Calendar, Assignments) use onSnapshot listeners to ensure data updates instantly across all users viewing the application.

