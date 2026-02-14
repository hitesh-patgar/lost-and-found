# Lost and Found Management System (Python Backend)

A backend-based Lost & Found Management System where users can register, login, report lost or found items, and search for matching items.  
The system stores item details in a database and helps users find lost items efficiently.

---

## Features
- User Registration
- User Login
- Report Lost Item
- Report Found Item
- View Lost Items
- View Found Items
- Search Items by Category and Location
- View Item Details with Contact Information

---

## Tech Stack
- Python (Backend)
- SQL
- MySQL Database

---

## Database Design

The project uses two tables: `users` and `items`.

---

### Table 1: Users

**Columns**
- `user_id` (Primary Key)
- `name`
- `email` (Unique)
- `password`
- `phone`
- `created_at`

**SQL Query**
```sql
CREATE TABLE users (
    user_id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(150) UNIQUE NOT NULL,
    password VARCHAR(100) NOT NULL,
    phone VARCHAR(15),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

### Table 2: Items(Main table)

**Columns**

- `item_id` (Primary Key)
- `item_name`
- `category`  (wallet, phone, bag)
- `description`
- `location`
- `date_reported`
- `status`  (Lost / Found)
- `contact_number`

**SQL Query**
```sql
"CREATE TABLE items (
    item_id INT PRIMARY KEY AUTO_INCREMENT,
    item_name VARCHAR(100) NOT NULL,
    category VARCHAR(50) NOT NULL,
    description TEXT,
    location VARCHAR(100),
    date_reported DATE,
    status VARCHAR(10) NOT NULL,
    contact_number VARCHAR(15),
    user_id INT,
    FOREIGN KEY (user_id) REFERENCES users(user_id)
);
"
