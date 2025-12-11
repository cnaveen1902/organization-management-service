# organization-management-service


Organization Management Service — Backend Assignment

This project is a backend service built using FastAPI, MongoDB Atlas, and JWT authentication.
It demonstrates a multi-tenant architecture where each organization gets its own dynamic MongoDB collection.

This backend supports:

Creating organizations

Admin authentication

Managing organization metadata

Updating organization (including dynamic collection renaming + migration)

Deleting organization safely with authentication

It also exposes a full Swagger UI for easy testing.

🚀 Features
✔ Create Organization

Validates that organization name is unique

Creates dynamic MongoDB collection (org_<slug>)

Creates admin user with hashed password

Stores org metadata in master database

✔ Admin Login

Validates email/password

Returns JWT token with admin ID + organization ID

✔ Get Organization

Fetch metadata from master DB

✔ Update Organization

Validates admin credentials

Creates new dynamic collection with updated name

Migrates existing organization data

Updates metadata

✔ Delete Organization

Requires JWT token

Deletes the organization + all admin + dynamic collection

| Component         | Technology         |
| ----------------- | ------------------ |
| Backend Framework | FastAPI            |
| Database          | MongoDB Atlas      |
| Auth              | JWT (python-jose)  |
| Hashing           | Passlib (bcrypt)   |
| Hosting (Colab)   | ngrok tunnel       |
| Web Docs          | Swagger UI `/docs` |

project structure
project/
│── main.py               # FastAPI backend implementation
│── README.md             # Documentation
│── requirements.txt      # Package list (optional)


