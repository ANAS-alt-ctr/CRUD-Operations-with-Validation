📦 Repository Overview

CRUD‑Operations‑with‑Validation GitHub Repo

This repository contains a simple Python project using FastAPI (a lightweight Python web framework) to implement CRUD operations (Create, Read, Delete) with basic validation.

There isn’t an official description in the repo itself, but the code tells us what it does:

🧠 What the Project Does

It builds a small API to manage a list of users stored in a users.json file. The available endpoints include:

✅ Read Users

GET / — Returns all users stored in users.json.

✅ Create User

POST /users — Adds a new user with fields like name, age, city, email, and review.

Uses Pydantic for input validation (e.g., valid email, required fields).

Also enforces that review isn’t empty and doesn’t exceed a length limit.

After validating, it writes the new user back to the JSON file and returns the created record.

✅ Delete User

DELETE /users/{user_id} — Removes a user by ID.

🔍 Analyze a User

GET /Analyze/{user_id} — Performs basic analysis of a user’s review text:

Word count

Number of uppercase letters

Number of special characters

Returns these metrics along with the user ID.

🛠️ Key Technologies

Python — Core language.

FastAPI — Web framework for building the API.

Pydantic — Used for validating input data.

JSON file (users.json) — Acts as simple persistent storage for user records.

🧩 Notes

Because this project uses a flat JSON file instead of a database, it’s mainly suitable for learning or small demo purposes.

FastAPI is designed to serve both simple and scalable APIs — this project shows a basic example focused on CRUD and validation.

🧑‍💻 How It Works in Practice

When you run the FastAPI server:

Start the server:

uvicorn main:app --reload

Visit http://localhost:8000/docs in a browser — FastAPI auto-generates interactive documentation for the API (Swagger UI) so you can test endpoints visually without external tools.
