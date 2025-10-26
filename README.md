# Basic Task Manager

A simple full-stack web application that allows users to create, view, update, and delete tasks.
This project is built as part of the PLC Home Coding Assignment (Task 1).

---

## Technologies Used

| Layer         | Technology                         |
| ------------- | ---------------------------------- |
| Frontend      | React + TypeScript (Vite)          |
| Backend       | ASP.NET Core 8 Web API (C#)        |
| Communication | REST API using Axios               |
| Data Storage  | In-memory repository (no database) |

---

## Features

* Add new tasks
* Mark tasks as complete or incomplete
* Delete tasks
* Simple user interface

---

## Folder Structure

```
basic-task-manager/
├─ backend/
│  └─ TaskApi/
│     ├─ Controllers/
│     │  └─ TasksController.cs
│     ├─ Models/
│     │  └─ TaskItem.cs
│     ├─ Repositories/
│     │  ├─ ITaskRepository.cs
│     │  └─ InMemoryTaskRepository.cs
│     ├─ Program.cs
│     └─ TaskApi.csproj
├─ frontend/
│  ├─ src/
│  │  ├─ api/tasks.ts
│  │  ├─ components/
│  │  │  ├─ AddTaskForm.tsx
│  │  │  └─ TaskList.tsx
│  │  ├─ App.tsx
│  │  └─ main.tsx
│  ├─ package.json
│  └─ tsconfig.json
└─ README.md
```

---

## Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/basic-task-manager.git
cd basic-task-manager
```

### 2. Backend Setup

```bash
cd backend/TaskApi
dotnet restore
dotnet build
dotnet run
```

The API will be available at:

* [http://localhost:5144](http://localhost:5000) (HTTP)

### 3. Frontend Setup

```bash
cd ../../frontend
npm install
npm run dev
```

The frontend will run at:
[http://localhost:5173](http://localhost:5173)

---

## API Endpoints

| Method | Endpoint          | Description       | Example Body                                                  |
| ------ | ----------------- | ----------------- | ------------------------------------------------------------- |
| GET    | `/api/tasks`      | Get all tasks     | -                                                             |
| GET    | `/api/tasks/{id}` | Get a single task | -                                                             |
| POST   | `/api/tasks`      | Create a task     | `{ "description": "Buy groceries" }`                          |
| PUT    | `/api/tasks/{id}` | Update a task     | `{ "id": 1, "description": "Buy milk", "isCompleted": true }` |
| DELETE | `/api/tasks/{id}` | Delete a task     | -                                                             |

---

## How It Works

1. The backend stores tasks in memory (no database required).
2. The frontend interacts with the backend through REST API calls using Axios.
3. Each action (add, update, delete) updates the in-memory task list and refreshes the UI.

---

##Screenshots
<img width="1908" height="858" alt="image" src="https://github.com/user-attachments/assets/7bcad2e4-2954-4586-bf6f-2d41cd4a5b11" />

<img width="1908" height="858" alt="image" src="https://github.com/user-attachments/assets/abf78f03-e0ea-4f58-b9e7-5615ecd3fe72" />
