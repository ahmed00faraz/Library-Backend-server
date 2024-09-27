# Library Backend Server

This is a Flask-based backend server that manages a collection of books. The application allows users to add, update, and delete book entries in an SQLite database. Each book has a title, author, and rating. 

## Features

- **View all books**: Displays all books in the collection.
- **Add a new book**: Users can add a book with a title, author, and rating.
- **Edit a book's rating**: Users can update the rating of a selected book.
- **Delete a book**: Users can delete a book from the collection.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/ahmed00faraz/Library-Backend-server.git
   cd Library-Backend-server
   ```

2. Set up a virtual environment and activate it:

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Run the Flask application:

   ```bash
   python app.py
   ```

5. Navigate to `http://127.0.0.1:5000/` in your browser to access the app.

## Endpoints

- `/` : Home page showing the list of all books in the collection.
- `/add` : Add a new book to the collection.
- `/edit` : Edit the rating of an existing book.
- `/delete` : Delete a book from the collection.

## Project Structure

```bash
Library-Backend-server/
│
├── templates/               # HTML templates for the web pages
│   ├── index.html           # Displays the list of books
│   ├── add.html             # Form to add a new book
│   └── edit_rating.html     # Form to edit a book's rating
│
├── app.py                   # Main Flask application file
├── requirements.txt         # Python dependencies
├── new-book-collections.db   # SQLite database file
└── README.md                # Project readme
```

## Database

The application uses an SQLite database named `new-book-collections.db`. The database consists of a single table `Book`, which stores the following fields:

- `id`: Integer, primary key, auto-incremented.
- `title`: String, unique, cannot be null.
- `author`: String, cannot be null.
- `rating`: Float, cannot be null.

You can create the database by running the Flask app. The database schema is generated automatically.

## Usage

1. **Add a new book**:
   - Go to the `/add` page to add a new book with a title, author, and rating.
   
2. **Edit book rating**:
   - Click on the "Edit" button next to any book to update its rating.
   
3. **Delete a book**:
   - Click on the "Delete" button next to any book to remove it from the collection.
