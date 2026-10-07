# Library API Design

A RESTful API specification for managing books in a library catalog system.

## Endpoints

### 1. List All Books (with optional Author filter)
* **Method:** `GET`
* **Path:** `/books` (or `/books?author=Jane+Austen`)
* **Description:** Retrieves a list of all library books, supporting filtering via a query parameter.
* **Success Status Code:** `200 OK`

### 2. Get One Book
* **Method:** `GET`
* **Path:** `/books/{id}`
* **Description:** Retrieves the complete details of a single book specified by its unique ID.
* **Success Status Code:** `200 OK`

### 3. Create a Book
* **Method:** `POST`
* **Path:** `/books`
* **Description:** Adds a new book entry to the library catalog.
* **Example Request Body:**
  ```json
  {
    "title": "Pride and Prejudice",
    "author": "Jane Austen",
    "publishedYear": 1813,
    "isbn": "978-0141439518"
  }