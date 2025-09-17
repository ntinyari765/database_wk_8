# Library Management System Database

A comprehensive MySQL database schema designed to manage library operations including book inventory, member management, loans, reservations, and fine tracking.

## Project Overview

This database system provides the foundation for a library management application. It handles core library operations such as:
- Managing book collections and author information
- Tracking library members and their borrowing privileges  
- Processing book loans and returns
- Managing book reservations
- Recording and tracking fines for overdue items

The schema is designed with proper normalization, referential integrity, and scalability in mind.

## Database Schema

The database consists of 8 interconnected tables:

### Core Tables
- **books**: Stores book information (title, ISBN, publication details, availability status)
- **authors**: Contains author details (name, biography, contact information)
- **publishers**: Publisher information (name, address, contact details)
- **members**: Library member profiles (personal details, membership status, contact info)

### Relationship Tables
- **book_authors**: Many-to-many relationship linking books to their authors
- **loans**: Tracks active and historical book borrowing records
- **reservations**: Manages book reservation requests from members
- **fines**: Records penalties for overdue books or damages

### Key Relationships
- Books can have multiple authors, and authors can write multiple books
- Members can borrow multiple books and have multiple loans over time
- Books can be reserved by multiple members (queue system)
- Fines are linked to specific loans and members

## How to Run the SQL File

### Prerequisites
- MySQL Server installed and running
- MySQL Workbench installed
- Administrative privileges to create databases

### Installation Steps

1. **Open MySQL Workbench**
   - Launch MySQL Workbench
   - Connect to your MySQL server instance

2. **Open the SQL File**
   - Go to `File` → `Open SQL Script`
   - Navigate to and select your `library_management.sql` file

3. **Execute the Schema**
   - Review the SQL script in the editor
   - Click the lightning bolt icon (⚡) or press `Ctrl+Shift+Enter` to execute all statements
   - Monitor the output panel for any errors or warnings

4. **Verify Installation**
   - Refresh the schema list in the Navigator panel
   - Confirm all 8 tables were created successfully
   - Check table structures and relationships in the EER diagram

### Alternative Method (Command Line)
```bash
mysql -u username -p
source /path/to/library_management.sql
```

*This database schema provides a solid foundation for library management operations and can be extended based on specific institutional requirements.*