This is a Java-based command-line Library Management System developed using Object-Oriented Programming (OOP) principles. The project is built in IntelliJ IDEA using Maven and models a real-world library system with functionalities for both librarians and members.

🚀 Features
🔐 Main Menu (on start):
1. Librarian Login

2. Member Login

3. Exit

👩‍🏫 Librarian Functions:
📌 Register a new member

❌ Remove a member

📚 Add a new book

🗑️ Remove a book

👥 View all members with borrowed books and fines

📖 View all books

🔙 Go back to main menu

🙋‍♂️ Member Functions:
🔐 Authenticate using name and phone number

📖 List available books

📘 View borrowed books

➕ Issue a book (Max 2 books, no issuing if fine exists)

🔁 Return a book (fine imposed if returned after 10 seconds)

💰 Pay fine

🔙 Go back to main menu

🔧 Input Validation & Error Handling
Validates phone number (must be 9 or 10 digits)

Validates age (must be > 0 and ≤ 130)

Handles incorrect input types (e.g., string instead of int) using custom getInt() and getLong() methods

Prevents duplicate member registration with same phone number

Prevents fine payment if no fine exists

Restricts issuing a second book if a fine is pending

🧱 Classes Overview
📘 Book Class
Attributes: bookID, title, author, totalCopies, borrowTime, returnTime

Constructor initializes book details

👤 Member Class
Attributes: memberID, name, age, phoneNumber, borrowedBooks, fine

Key Methods:

borrowBook(), retb(), updatef(), pf(), listbook(), rb(), tfine(), checks()

🏛️ Library Class
Maintains lists:

BOOK: List of all books

MEM: List of all members

Key Methods:

addBook(), removeBook(), registerMem(), removeMem(), listBook(), listMem(), enterAsMem()

Contains static counters and utility functions for input checking

🛑 Exit Strategy
To exit the program, choose Option 3 from the main menu

Invalid inputs are handled gracefully with prompts, ensuring the program does not crash unexpectedly

💻 Tech Stack
Java (JDK 8+)

Maven for project management

IntelliJ IDEA as the development environment

Command-line interface for user interaction

📎 Notes
A fine is calculated if a book is returned after 10 seconds of issuing

Members can borrow at most 2 books at a time

The system ensures robust input validation and simulates a real-life library workflow
