# Bookflow - Database Project

This project implements a database schema for a bookstore management system called "Bookflow". It includes tables for managing books, customers, orders, and more. The project also features views, stored procedures, functions, and triggers to support various functionalities of the application.

## Database Schema

The database is named `Bookflow` and uses the `utf8mb4` character set.

### Tables

* **Categorias**: Stores book categories.
* **Livros**: Contains information about the books, including title, author, ISBN, price, and stock quantity.
* **Autores**: Stores information about the authors.
* **Editoras**: Contains the names of the publishers.
* **Clientes**: Manages customer data, such as name, email, and address.
* **Pedidos**: Stores customer orders, including order date and status.
* **Itens_Pedido**: Contains the individual items for each order.
* **Carrinho**: Manages the items in each customer's shopping cart.

## Features

### Views

* `vw_livros_mais_vendidos`: A view that lists the best-selling books.
* `vw_estoque_baixo`: Shows books with low stock (less than 10 units).
* `vw_clientes_ativos`: Lists customers who have placed an order in the last 6 months.
* `vw_relatorio_vendas`: A sales report grouped by category and author.

### Stored Procedures

* `cadastrar_cliente`: Registers a new customer.
* `atualizar_cliente`: Updates a customer's information.
* `excluir_cliente`: Deletes a customer.
* `criar_pedido`: Creates a new order for a customer.
* `adicionar_item_pedido`: Adds a book to an order and updates the stock.
* `atualizar_status_pedido`: Updates the status of an order.

### Functions

* `login_cliente`: Validates a customer's login credentials.
* `recuperar_senha`: Retrieves a customer's password.
* `calcular_total_pedido`: Calculates the total cost of an order, including shipping and taxes.

### Triggers

* `verificar_estoque`: A trigger that checks if there is enough stock before adding a book to an order.

### Indexes

The database includes several indexes on the tables to improve query performance, especially on foreign keys and frequently filtered columns.

## How to Use

1.  **Database Setup**: Execute the `Database/Tables.sql` script to create the database and tables, and to insert the initial data.
2.  **Install Additional Features**: Run the scripts in the `Database` folder to create the views, procedures, functions, triggers, and indexes.

## Sample Queries

The `Database/Tables.sql` file also contains several sample `SELECT` queries that demonstrate how to retrieve information from the database, such as:

* Selecting books with a price above a certain value.
* Listing books from a specific category.
* Finding orders with a specific status.
* Calculating the total value of an order.
