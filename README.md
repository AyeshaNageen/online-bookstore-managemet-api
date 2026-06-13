# Online Bookstore Management API

A RESTful backend API built with Node.js, Express, and MongoDB for managing books in an online bookstore.

## Features

- Add, view, update, and delete books
- MongoDB/Mongoose book schema
- Request logging middleware
- Global JSON error handler
- Search by author and genre
- Pagination for large book lists
- JSON request and response format

## Project Structure

```text
online-bookstore-api/
├── models/
│   └── Book.js
├── routes/
│   └── books.js
├── docs/
│   └── Online Bookstore API.postman_collection.json
├── .env
├── .gitignore
├── package.json
├── README.md
└── server.js
```

## Setup

1. Install dependencies:

```bash
npm install
```

2. Configure environment variables in `.env`:

```env
PORT=5000
MONGODB_URI=mongodb://127.0.0.1:27017/online_bookstore
```

For MongoDB Atlas, replace `MONGODB_URI` with your Atlas connection string. Do not publish real credentials publicly.

3. Start the server:

```bash
npm start
```

For development with nodemon:

```bash
npm run dev
```

## API Endpoints

Base URL:

```text
http://localhost:5000
```

| Method | Endpoint | Description |
| --- | --- | --- |
| GET | `/api/books` | Get all books |
| GET | `/api/books/:id` | Get one book by ID |
| POST | `/api/books` | Add a new book |
| PUT | `/api/books/:id` | Update an existing book |
| DELETE | `/api/books/:id` | Delete a book |

## Search And Pagination

Search by author and genre:

```text
GET /api/books?author=John&genre=fiction
```

Paginate results:

```text
GET /api/books?page=1&limit=10
```

Search and paginate together:

```text
GET /api/books?author=John&genre=fiction&page=1&limit=5
```

## Example Request Body

```json
{
  "title": "Clean Code",
  "author": "Robert C. Martin",
  "genre": "Programming",
  "price": 25.99,
  "publishedDate": "2008-08-01",
  "inStock": true
}
```

## Status Codes

- `200` success
- `201` created
- `400` bad request or validation error
- `404` route or book not found

## Submission Notes

- Include the GitHub repository link in Google Classroom private comments.
- Include the live API URL if deployed.
- Import `docs/Online Bookstore API.postman_collection.json` in Postman to test all routes.

