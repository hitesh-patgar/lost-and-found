# lost-and-found

# database
there are two tables user and items 

-> TABLE 1: USERS

Columns:

user_id (Primary Key)

name

email (Unique)

password

phone

created_at

sql query "CREATE TABLE users (
    user_id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100) NOT NULL,
    email VARCHAR(150) UNIQUE NOT NULL,
    password VARCHAR(100) NOT NULL,
    phone VARCHAR(15),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
"

-> TABLE 2 : ITEMS (MAIN TABLE)

Columns:

item_id (Primary Key)

item_name

category (wallet, phone, bag)

description

location

date_reported

status (Lost / Found)

contact_number

user_id (Foreign Key from users table)
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
