# 🧩 Associate Software Engineer Assessment – Task Management System

This project was developed as part of the **Associate Software Engineer (Python + React)** assessment.  
It consists of two main parts:  
- **Task #1 (Backend)** – Building backend APIs for managing comments using CRUD operations.  
- **Task #2 (Frontend)** – Creating a user interface for managing tasks using existing APIs.

---

## 🧠 Task #1: Backend – Comment Management API

The backend focuses on **creating, reading, updating, and deleting (CRUD)** comments for specific tasks.

### 🔹 Purpose
The goal was to design RESTful APIs that allow users to:
- Add a comment to a task.
- Edit an existing comment.
- Delete a comment.
- Retrieve all comments related to a specific task.

Each operation follows **CRUD principles**, ensuring clear and predictable data flow between the client and server.

### 🔹 How It Works
- When a comment is added, it is linked to a particular task using its task ID.
- Each comment includes timestamps (`createdAt`, `updatedAt`) to track activity.
- The API includes **input validation**, ensuring that empty or invalid comments are rejected.
- **Error handling** is implemented for missing tasks, invalid IDs, and failed requests.

### 🔹 Automated Testing
To verify API functionality, a **test runner** was created that:
- Automatically executes a series of CRUD tests on all API endpoints.
- Displays the results visually, showing which tests passed or failed.
- Measures test performance, success rate, and total execution time.
- Tests include:
  - Health check endpoint verification.
  - Task creation and retrieval (GET, POST).
  - Comment operations (GET, POST, PUT, DELETE).
  - Validation for invalid input or missing data.
  - 404 handling for non-existent resources.
  - Timestamp verification (createdAt and updatedAt fields).

If all tests pass successfully, the interface displays a message confirming that the Comment API is working correctly.

---

## ⚛️ Task #2: Frontend – Task Management Interface

The frontend is built using **React.js** and provides an interactive UI for managing tasks.  
It connects with the existing APIs to perform the following operations:
- ➕ Add new tasks  
- 🖊️ Edit existing tasks  
- ❌ Delete tasks  
- 📋 View all tasks categorized by status (To Do, In Progress, Completed)

### 🔹 Core Features
1. **Task Loading** – When the application starts, it automatically loads all tasks using an API call and displays them under different tabs (All, To Do, In Progress, Completed).  
2. **Add Task** – Users can open a dialog to create a new task by entering a title, description, and status.  
3. **Edit Task** – Tasks can be updated easily by clicking the “Edit” option, opening a pre-filled dialog.  
4. **Delete Task** – Tasks can be deleted after confirmation in a pop-up dialog.  
5. **Dynamic Tabs** – Each task status has its own section, allowing smooth navigation.  
6. **Notifications** – The interface provides success and error toasts (messages) for user actions such as task creation, updates, or deletions.  

### 🔹 How It Works
- The **useState** hook manages all dynamic data such as tasks, dialogs, and active tabs.  
- The **useEffect** hook is used to fetch data automatically when the page loads or when updates occur.  
- The app interacts with API functions such as:
  - `getTasks()` – to retrieve tasks from the server  
  - `createTask()` – to add a new task  
  - `updateTask()` – to modify an existing task  
  - `deleteTask()` – to remove a task  

These APIs are integrated with visual components like:
- **TaskDialog** for adding or editing a task  
- **DeleteTaskDialog** for confirming task deletion  
- **Tabs** for switching between task categories  

### 🔹 User Interface
The UI has a clean and modern layout:
- A **header** with a “New Task” button and project title.  
- **Tabs** for filtering tasks by status.  
- **Dialogs** for creating and editing tasks.  
- **Loading animation** when data is being fetched.  
- **Success and error toasts** to keep the user informed.  

---

## 🔍 Summary of Key Learnings
- Designed **RESTful APIs** with full CRUD support for managing comments.  
- Implemented **automated testing** to verify backend functionality.  
- Built an interactive **React frontend** with task filtering, editing, and deletion.  
- Improved user experience with real-time UI updates, dialogs, and notifications.  

---

## 🧩 Technologies Used
- **Backend:** Python, Flask, Supabase Functions  
- **Frontend:** React.js, TypeScript, Lucide React Icons  
- **UI Components:** Shadcn/UI, Sonner Notifications  
- **Testing Framework:** Custom automated test runner for API validation  

---

## ✨ Conclusion
This project demonstrates a complete **full-stack development workflow** — from backend API creation and testing to frontend integration and user interface design.  
It highlights strong understanding of CRUD operations, API handling, state management, and clean UI development.

---

🔗 **GitHub Repository:**  
*(https://github.com/shilpa20031308/Python-React-Assessment)*
