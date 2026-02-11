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
