# TaskFlow

TaskFlow is a robust and user-friendly Task Management System built with Django. It provides a clean interface for users to manage their daily tasks with full CRUD (Create, Read, Update, Delete) functionality. Each user has a personalized view of their own tasks, ensuring data privacy and organization.

## Features

-   **User Authentication**: Secure Login, Registration, and Logout functionality.
-   **Personalized Dashboard**: Users can only view and manage their own tasks.
-   **Task Management**:
    -   **Create**: Add new tasks with titles and detailed descriptions.
    -   **Read**: View a list of pending and completed tasks.
    -   **Update**: Edit task details or mark them as complete/incomplete.
    -   **Delete**: Remove tasks that are no longer needed.
-   **Search Functionality**: Easily search through tasks (codebase reference: `TaskContext` filtering).
-   **Responsive Design**: Clean and simple UI using Django templates.

## Tech Stack

-   **Backend**: [Django 5.2.4](https://www.djangoproject.com/) (Python Web Framework)
-   **Database**: SQLite (Default Django database, easy to switch to PostgreSQL/MySQL)
-   **Frontend**: HTML5, CSS3, Django Template Language (DTL)
-   **Utilities**: `django-contrib-auth` for authentication.

## Screenshots

### Login Page
Secure entry point for users.
![Login Page](screenshots/login.png)

### Task List (Dashboard)
Overview of all tasks with status indicators.
![Task Dashboard](screenshots/create_task.png)

### Task Details
View and edit specific information about a task.
![Task Details](screenshots/task_details.png)

### Delete Confirmation
Safety check before removing a task.
![Delete Task](screenshots/delete_task.png)

## Installation & Setup

Follow these steps to get a local copy of the project up and running.

### Prerequisites

-   Python 3.10+ installed on your machine.
-   Git for cloning the repository.

### Installation

1.  **Clone the repository**
    ```bash
    git clone <repository-url>
    cd todo_list
    ```

2.  **Create a Virtual Environment**
    It is recommended to use a virtual environment to manage dependencies.
    ```bash
    python -m venv .venv
    # Activate on Mac/Linux
    source .venv/bin/activate
    # Activate on Windows
    # .venv\Scripts\activate
    ```

3.  **Install Dependencies**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Apply Migrations**
    Set up the database schema.
    ```bash
    python manage.py migrate
    ```

5.  **Create a Superuser (Optional)**
    To access the Django Admin panel.
    ```bash
    python manage.py createsuperuser
    ```

6.  **Run the Server**
    ```bash
    python manage.py runserver
    ```

    Open your browser and navigate to `http://127.0.0.1:8000/`.

## Project Structure

```text
todo_list/
├── base/                  # Core application directory
│   ├── migrations/        # Database migrations
│   ├── templates/base/    # HTML templates (login, register, task_list, etc.)
│   ├── models.py          # Database models (Task)
│   ├── views.py           # Application logic and views
│   ├── urls.py            # URL routing for the base app
│   └── ...
├── todo_list/             # Project configuration
│   ├── settings.py        # Global settings
│   ├── urls.py            # Main URL routing
│   └── ...
├── screenshots/           # Images for README
├── db.sqlite3             # SQLite Database
├── manage.py              # Django command-line utility
└── requirements.txt       # Python dependencies
```
