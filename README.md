# Database-GroupProject
# Bookstore Database System 📚

A comprehensive MySQL database solution for managing bookstore operations, including inventory, customers, orders, and shipping. Designed for scalability and real-world use.

## Features ✨
- *Multi-country Support*: Track customers across Kenya, USA, UK, and Nigeria
- *Inventory Management*: Books, authors, publishers, and language tracking
- *Order Processing*: Full order lifecycle from placement to delivery
- *Address History*: Track current/previous customer addresses
- *Security*: Role-based access control (Admin vs Read-Only users)

## Tech Stack 🛠
- *Database*: MySQL 8.0+
- *Visualization*: Draw.io/MySQL Workbench
- *Query Interface*: MySQL Workbench/CLI

## Database Schema 📊
### Core Tables
| Table | Description |
|-------|-------------|
| book | Stores book details (ISBN, price, publication date) |
| author | Author information with support for multiple names |
| cust_order | Order records with shipping method links |
| customer_address | Manages multiple addresses per customer |

### Relationships
```sql
Customer 1───┐
             ├── customer_address ─── address
AddressStatus ┘

book ── book_author ── author
cust_order ── order_line ── book
