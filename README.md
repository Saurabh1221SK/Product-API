# Product API

A REST API built with Node.js, Express, and MySQL for managing product data. I built this project to practice backend development, database integration, REST API design, and CRUD operations.

## Features

* Create, view, update, and delete products
* Fetch all products or a single product by ID
* MySQL connection pooling using `mysql2`
* Environment-based database configuration
* Basic request validation
* Error handling with appropriate HTTP status codes
* Modular project structure using routes and controllers

## Tech Stack

**Backend:** Node.js, Express.js
**Database:** MySQL
**Packages:** mysql2, dotenv
**Testing:** Postman

## Project Structure

```text
Product-API/
├── config/
│   └── db.js
├── controllers/
│   └── productController.js
├── routes/
│   └── productRoutes.js
├── db_script.sql
├── index.js
├── package.json
└── package-lock.json
```

## Setup

Clone the repository and install dependencies:

```bash
git clone git@github.com:Saurabh1221SK/Product-API.git
cd Product-API
npm install
```

Create a `.env` file:

```env
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_password
DB_NAME=product_db
```

Run `db_script.sql` in MySQL to create the database and products table.

Start the server:

```bash
npm start
```

The API runs locally on port `8090`.

## API Endpoints

| Method | Endpoint | Description          |
| ------ | -------- | -------------------- |
| GET    | `/`      | Get all products     |
| GET    | `/:id`   | Get a product by ID  |
| POST   | `/`      | Create a new product |
| PUT    | `/:id`   | Update a product     |
| DELETE | `/:id`   | Delete a product     |

## Example Product

```json
{
  "name": "Activa scooty",
  "price": 100000,
  "description": "A high-end scooty"
}
```

## What I Learned

This project helped me understand how an Express application communicates with a MySQL database, how CRUD operations map to HTTP methods and SQL queries, and how to organize backend code using separate configuration, controller, and route layers.
