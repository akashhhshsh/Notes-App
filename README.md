# 📝 Smart Notes App - FastAPI & MongoDB

## 📌 Overview
Smart Notes is a simple **Notes-Keeping App** built using **FastAPI** (Python's modern web framework) and **MongoDB** as the database. It allows users to add, view, and categorize notes as **important** or **normal**.

## 🚀 Tech Stack
- **FastAPI** - High-performance backend framework  
- **MongoDB** - NoSQL database for storing notes  
- **Jinja2** - Templating engine for rendering HTML  
- **Bootstrap** - For styling and responsive UI  

---

## 🛠️ Project Structure & Flow

### 1️⃣ **Database Connection** (`db.py`)
- Uses `pymongo` to connect to MongoDB.
- `MongoClient` connects to the database.

### 2️⃣ **Data Model** (`models/note.py`)
- Uses **Pydantic** to define a `Note` model with:
  - `title`: The note's title  
  - `desc`: The note's description  
  - `important`: Boolean flag for marking notes as important  

### 3️⃣ **Routes & API Logic** (`routes/note.py`)
- **GET `/`**: Fetches all notes from MongoDB and passes them to the HTML template.
- **POST `/`**: Takes form input, processes it, and inserts a new note into the database.

### 4️⃣ **Schema Definition** (`schemas/note.py`)
- Converts MongoDB objects into a **Python dictionary**.
- Helps format the notes before sending them to the frontend.

### 5️⃣ **Frontend & Templates**
- **`templates/index.html`**: Uses Jinja2 to render notes dynamically.
- **Bootstrap** is used for a modern, mobile-friendly design.

### 6️⃣ **Main Entry Point** (`index.py`)
- Initializes **FastAPI**.
- Mounts static files (`style.css`).
- Includes the `note` router for handling note operations.

---

## 📸 Screenshots
<img width="1440" alt="Screenshot 2025-02-13 at 3 33 28 AM" src="https://github.com/user-attachments/assets/2cd83af3-b359-4bff-8dde-fd25be745aff" />
<img width="1440" alt="Screenshot 2025-02-13 at 3 01 52 AM" src="https://github.com/user-attachments/assets/c5ed09b2-65f5-4c05-9929-b6ec5144b991" />


  
  

---

## 🏗️ Installation & Running Locally
1. **Clone the Repository**
   ```sh
   git clone https://github.com/yourusername/smart-notes-app.git
   cd smart-notes-app

## Install Dependencies
   ```sh
pip install fastapi pymongo uvicorn jinja2
```
## Run the App
```sh
uvicorn index:app --reload
```
## Visit in Browser
```sh
http://127.0.0.1:8000
```

## 🌟 Features
✅ Add new notes with a title & description
✅ Mark notes as important or normal
✅ Responsive UI with Bootstrap
✅ Fetch & display notes dynamically
