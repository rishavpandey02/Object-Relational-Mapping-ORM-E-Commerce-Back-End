# E-commerce Backend ORM

This backend solution uses an Object Relational Mapping (ORM) approach to connect and interact with a MySQL database using Sequelize and Express.js. Below you will find instructions on how to set up, seed, and run the application.

## Acceptance Criteria

1. **Environment Configuration**
    - Connect to the database using Sequelize.
    - Configure your database name, MySQL username, and MySQL password in an environment variable file.

2. **Database Setup**
    - Running specific commands will create a development database.
    - Seed this database with test data for development purposes.

3. **Server Initialization**
    - Invoke a specific command to start the server.
    - Upon server start, Sequelize models sync to the MySQL database.

4. **API Endpoints**
    - Test various API GET routes using Insomnia for categories, products, or tags.
    - The returned data for each endpoint will be in formatted JSON.
    - POST, PUT, and DELETE routes can be tested to create, update, or delete data in the database respectively.

## Setup Instructions

### Prerequisites

- Node.js
- MySQL
- A tool for testing API endpoints, such as Insomnia.

### Installation

1. Clone the repository to your local machine.
2. Navigate to the root directory in your terminal.
3. Install necessary dependencies using the following command:
    ```bash
    npm install
    ```

### Database Configuration

1. Open your MySQL shell and log in.
2. Create a new database for this application.
3. In the root directory, create a `.env` file and add the following configurations:
    ```env
    DB_NAME=<your_database_name>
    DB_USER=<your_MySQL_username>
    DB_PW=<your_MySQL_password>
    ```

### Seed the Database

1. Navigate to the root directory in your terminal.
2. To create tables in your database, run the schema command:
    ```bash
    source db/schema.sql
    ```
3. Seed the created tables with test data using the seed command:
    ```bash
    npm run seed
    ```

### Starting the Server

1. To start the server, run the following command in your terminal:
    ```bash
    npm start
    ```
2. Upon success, you will see a message indicating the server is running and Sequelize models have synced to the MySQL database.

### Testing API Endpoints

Using Insomnia:

1. Test GET routes for:
    - Categories: `<your_server_address>/api/categories`
    - Products: `<your_server_address>/api/products`
    - Tags: `<your_server_address>/api/tags`

2. Test POST, PUT, and DELETE routes as necessary for creating, updating, or deleting data.

## Conclusion

You now have a functional ORM for an e-commerce backend! Always ensure you follow best practices for securing your database and sensitive information.
