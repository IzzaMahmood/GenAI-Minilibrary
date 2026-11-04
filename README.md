# Mini Library Management System
Mini Library Management System
A beginner-friendly, browser-based library management project built with
HTML, CSS, and vanilla JavaScript. The project provides six separate
pages for managing a small collection of books: dashboard, adding books,
editing and deleting books, searching, issuing, and returning books.


Table of Contents
- Project Overview
- Team Members and
  Responsibilities
- Project Structure
- Features
- Technologies Used
- Possible Future Improvements


Project Overview
The Mini Library Management System is designed to help a small library
maintain a basic collection of books. Users can add books, update or
remove existing records, search the collection, issue available books to
borrowers, and record their return.

The application is divided into six standalone HTML pages. Each page
contains its own:
- HTML for page structure and forms.
- CSS inside a <style> element for layout and visual styling.
- JavaScript inside a <script> element for page behaviour and
  data handling.
All six pages use the same browser localStorage key,
miniLibraryBooks, to read and save the book collection. No external
libraries, frameworks, backend server, or database are included.


Team Members and Responsibilities
  Team member   Responsibility                     File
  Alisha        Dashboard and collection summary   dashboard.html
Hajra         Add new books                      add_books.html
Memoona       Edit and delete book records       edit_delete_books.html
Izza          Search the book collection         search_books.html
Sitwat        Issue books to borrowers           issue_books.html
Zubaida       Record returned books              return_books.html



Project Structure
Keep all six files in the same folder so the navigation links
between pages work correctly.
mini-library-management-system/
├── dashboard.html
├── add_books.html
├── edit_delete_books.html
├── search_books.html
├── issue_books.html
├── return_books.html
└── README.md
There are no separate css/, js/, image, or configuration folders in
the current version. The CSS and JavaScript for each page are embedded
in that page's HTML file.


Features
1. Dashboard --- Alisha
File: dashboard.html
- Displays the total number of books.
- Displays how many books are available.
- Displays how many books are currently issued.
- Shows a table of book IDs, titles, authors, and statuses.
- Displays an empty-state message when the collection has no books.
The dashboard calculates its figures from the saved book records when
the page loads.

2. Add Books --- Hajra
File: add_books.html
- Adds a book to the collection.
- Collects the book title and author name (both required).
- Also accepts an optional category and ISBN.
- Assigns a generated ID using Date.now().
- Sets the new book's initial status to Available.
- Clears the form and displays a success message after saving.
  
3. Edit and Delete Books --- Memoona
File: edit_delete_books.html
- Loads existing books into a selection list.
- Displays the selected book's title, author, category, and ISBN.
- Saves changes to the selected book.
- Deletes a selected book after a confirmation prompt.

4. Search Books --- Izza
File: search_books.html
- Searches as the user types.
- Matches text in the title, author, category, and ISBN fields.
- Ignores letter case and leading/trailing spaces in the search term.
- Displays matching records with their current availability status.
- Shows a message when no books match.

5. Issue Books --- Sitwat
File: issue_books.html
- Lists only books whose status is Available.
- Collects the borrower's name and issue date.
- Changes the selected book's status to Issued.
- Stores the borrower's name and issue date with the book record.
- Removes the issued book from the available-books selection after
  saving.
  
6. Return Books --- Zubaida
File: return_books.html
- Lists books whose status is Issued.
- Shows the borrower and issue date for the selected book.
- Changes the book's status back to Available.
- Clears the borrower and issue-date fields after return.
- Removes the returned book from the issued-books selection.


Technologies Used
  Technology                          Purpose
  HTML5                               Page structure, forms, navigation,
and tables

  CSS3                                Styling, layout, responsive
adjustments, and visual feedback

  JavaScript (vanilla)                Form handling, searching, book
operations, and dashboard
calculations


  
Project Scope
The current release demonstrates the basic Create, Read, Update, and
Delete (CRUD) operations for book records, together with simple issue
and return status changes. It is intended for learning and demonstration
purposes.
