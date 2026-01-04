Library Book Management System

A full-stack Library Book Management System built using MongoDB, Express.js, Node.js, and React (Vite).
The application supports complete CRUD operations with validations, schema design, and robust error handling.
Books can be added, viewed, updated, filtered, and deleted with secure business-rule enforcement such as preventing negative stock and blocking deletion unless stock is zero. 



 Features

Add new book records
View all books
Filter books by category & publication year
Update available copies (increase / decrease)
Prevent negative stock
Delete only when available copies = 0
API error handling & validation
CRUD tested using Postman & MongoDB Shell
Clean and responsive React UI

Tech Stack
Frontend

React (Vite)

Fetch / Axios

HTML / CSS / JS

Backend

Node.js

Express.js

MongoDB

Mongoose

CORS

dotenv

Nodemon

Tools

Postman (API Testing)

MongoDB Shell

VS Code



Project Structure (Conceptual)
library-management-system/
 ├── backend/
 │   ├── models/
 │   ├── routes/
 │   ├── server.js
 │   └── .env
 ├── frontend/
 │   ├── src/
 │   ├── components/
 │   └── App.jsx
 └── README.md

 API Endpoints
 Insert Books
POST /api/books/seed


Adds multiple books at once & prevents duplicates.

 Get All Books
GET /api/books

 Get Books by Category
GET /api/books/category/:category

 Get Books Published After 2015
GET /api/books/after/2015

Update Available Copies
PATCH /api/books/:id/copies


Prevents negative stock

Delete a Book
DELETE /api/books/:id


Only allowed when available copies = 0



 Error Handling Cases

The system gracefully handles:

 Book not found
 Invalid update
 Negative stock attempts
 Delete request while copies remain

All verified via Postman & MongoDB Shell.




 Frontend UX

 Displays books in a card-based layout
 Includes forms for adding & editing books
  Fetches data on load
 Shows user-friendly success & error messages
 Basic responsive styling



 Conclusion

This project demonstrates a complete MERN-style full-stack workflow, including:

 CRUD implementation
 Database schema design
 API validation
 Error handling
 Real-world testing practices
