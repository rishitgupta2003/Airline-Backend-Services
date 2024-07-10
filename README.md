
---

# Airline Backend System

This project is a microservice-based backend system for an airline. It leverages various technologies and dependencies to provide a robust and scalable solution.

## Dependencies

### Core Dependencies

- **dotenv**: `^16.4.5` - Loads environment variables from a `.env` file into `process.env`.
- **express**: `^4.19.2` - A minimal and flexible Node.js web application framework.
- **http-status-codes**: `^2.3.0` - Utility to interact with HTTP status codes.
- **mysql2**: `^3.10.1` - A MySQL client for Node.js with a focus on performance.
- **nodemon**: `^3.1.4` - A tool that helps develop Node.js applications by automatically restarting the node application when file changes are detected.
- **sequelize**: `^6.37.3` - A promise-based Node.js ORM for various databases.
- **sequelize-cli**: `^6.6.2` - Command line tools for Sequelize.
- **winston**: `^3.13.0` - A logging library for Node.js.

### Additional Dependencies

- **amqplib**: `^0.10.4` - A library for RabbitMQ.
- **axios**: `^1.7.2` - A promise-based HTTP client for the browser and Node.js.
- **cron**: `^3.1.6` - A library for running cron jobs.
- **jsonwebtoken**: `^9.0.2` - A library for JSON Web Tokens.
- **node-cron**: `^3.0.3` - A library for running cron jobs in Node.js.
- **bcrypt**: `^5.1.1` - A library to help you hash passwords.
- **zod**: `^3.23.8` - A TypeScript-first schema declaration and validation library.

## Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/rishitgupta2003/Airline-Backend-Services.git
    cd Airline-Backend-Services
    ```

2. **Install dependencies**:
    ```bash
    npm install
    ```

3. **Set up environment variables**:
    - Create a `.env` file in the root directory of your project.
    - Add the necessary environment variables (e.g., database credentials, JWT secret).

4. **Run migrations**:
    ```bash
    npx sequelize-cli db:migrate
    ```

## Usage

1. **Start the server**:
    ```bash
    npm start
    ```

2. **Development mode** (with nodemon):
    ```bash
    npm run dev
    ```

## Project Structure

- **`config/`**: Contains configuration files, such as database configuration.
- **`migrations/`**: Contains Sequelize migration files.
- **`models/`**: Contains Sequelize models.
- **`routes/`**: Contains Express route handlers.
- **`controllers/`**: Contains business logic for handling requests.
- **`services/`**: Contains services for handling specific logic, such as authentication, scheduling, etc.

## Features

- **User Authentication**: Uses JWT for authentication and bcrypt for password hashing.
- **Database ORM**: Sequelize is used for database interactions.
- **Scheduled Tasks**: Cron jobs managed by `cron` and `node-cron`.
- **Messaging**: RabbitMQ integration via `amqplib`.
- **Logging**: Application logging using Winston.
---