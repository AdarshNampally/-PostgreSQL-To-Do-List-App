Preview:

![image](https://github.com/user-attachments/assets/81005bb5-3e40-4b4e-a483-e91f6c8d17b8)

![Screenshot 2025-06-19 192348](https://github.com/user-attachments/assets/3fd70d05-db0d-4d75-b4c7-20135034ba86)

🚀 Features:
✅ Create new tasks with a simple form

📋 Read and display all tasks from the PostgreSQL database

📝 Update task titles directly from the frontend using an inline edit form

❌ Delete tasks by checking the checkbox beside them

💾 Persistent storage using PostgreSQL (data survives server restarts)

🔄 All operations update the database in real-time and reload the UI seamlessly



🛠️ Tech Stack:


| Layer             | Technology                                                                                        |
| ----------------- | ------------------------------------------------------------------------------------------------- |
| Backend Server    | [Node.js](https://nodejs.org/) + [Express.js](https://expressjs.com/)                             |
| Database          | [PostgreSQL](https://www.postgresql.org/) with [pg](https://www.npmjs.com/package/pg) node module |
| Templating Engine | [EJS](https://ejs.co/)                                                                            |
| Styling           | Custom CSS (via `public/`)                                                                        |
| Forms & Logic     | HTML + JavaScript                                                                                 |




🧠 How It Works:
1. Homepage (GET /)

->Fetches all tasks from the items table in the PostgreSQL database.

->Renders them using index.ejs.

2. Add Task (POST /add)

->Takes the input from the form.

->Inserts the task into the items table.

->Redirects back to / to show updated list.

3. Delete Task (POST /delete)

->Triggered by checking the checkbox next to a task.

->Sends the task ID to the backend, deletes it from the database.

->Redirects back to /.

4. Edit Task (POST /edit)

->Clicking the pencil icon reveals an input field to edit the task title.

->Submitting the form updates the title in the database using the task's ID.

5. Frontend Logic  

->Minimal JavaScript handles toggling visibility between view/edit states.

->Each task item includes forms for delete and update, styled and positioned clearly.



🗂️ Database Schema:

The app uses a simple items table:\
CREATE TABLE items (\
  id SERIAL PRIMARY KEY,\
  title TEXT NOT NULL\
);




📚 Concepts Demonstrated:

Full stack app integration

RESTful routes using Express

PostgreSQL CRUD operations

Form handling in HTML + EJS

Separation of concerns (routes, views, logic)

Secure parameterized queries using pg module


