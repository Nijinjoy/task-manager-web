Project Overview
This project is a Task Management System built using Node.js,React js, Express, and SQLite. It allows users to create, update, and manage their tasks efficiently.

Setup & Installation
Clone the Repository:

bash
Copy
Edit
git clone <repository_url>
cd <project_folder>
Install Dependencies:

bash
Copy
Edit
npm install
Database Setup:

The project uses SQLite as the database.
Ensure the database file (database.sqlite) is correctly set up.
If using Sequelize ORM, run migrations:
bash
Copy
Edit
npx sequelize-cli db:migrate
Run the Server:

bash
Copy
Edit
npm start
The API will be available at http://localhost:5000.

Development Assumptions
Each task is linked to a user via userId.
The task status can be either "pending" or "completed".
The request body for creating a task must include title, description, userId, and status.
The database is SQLite, ensuring a lightweight and easy-to-manage data structure.
Authentication is implemented .
Technologies & Libraries Used
Backend: Node.js with Express.js
Database: SQLite
ORM: Sequelize
Middleware:
cors (for handling cross-origin requests)
dotenv (for managing environment variables)
express.json() (for parsing JSON requests)

Additional features
Included a dashboard that shows a summary (e.g., total tasks, pending tasks,
completed tasks).

Challenges & Solutions

Ensuring required fields are present when creating a task → Implemented input validation in the createTask controller.
Handling database schema changes → Used Sequelize migrations for structured schema management.
Preventing duplicate tasks → Added necessary constraints to maintain data integrity.
Consistent status field values → Used an ENUM type to allow only "pending" or "completed".
Fetching and merging tasks from both API and local storage → Implemented logic to avoid duplicates while combining stored and fetched tasks.
Managing state updates after creating or updating tasks → Used React state updates and useEffect to reflect changes dynamically.
Ensuring smooth navigation and data persistence → Used React Router’s useNavigate and localStorage for managing navigation and task persistence.
