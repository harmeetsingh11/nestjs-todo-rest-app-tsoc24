# NestJS Todo REST API

Welcome to the NestJS Todo REST API project. This application provides a robust, `RESTful` API for managing todos and tasks, complete with user authentication. Built using modern technologies like `NestJS`, `Prisma`, `PostgreSQL`, `Swagger`, and `TypeScript`, this project is designed for scalability and ease of use.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [API Endpoints](#api-endpoints)
- [Live Swagger API](#live-swagger-api)
- [Tech Stack](#tech-stack)
- [Installation & Setup](#installation--setup)
- [Running the Application](#running-the-application)
- [Testing the API](#testing-the-api)

## Project Overview

This is a Todo RESTful API application built as part of the [Timechain Summer of Code](https://tsoc.dev/) (TSoC'24) program. It provides a simple and effective way for users to manage their tasks with user authentication features. Users can create, read, update, and delete their tasks, with all data securely managed in a PostgreSQL database.

## Features

- User Authentication (Register/Login)
- CRUD operations for Todos/Tasks
- Swagger API documentation
- Type-safe code with TypeScript
- Seamless integration with PostgreSQL via Prisma
- Supports API testing with ThunderClient and Postman

## API Endpoints

### Todo

- **POST** `/todo` - Create a new Todo/Task
- **GET** `/todo` - Retrieve all of the user's Todos/Tasks
- **GET** `/todo/{id}` - Retrieve a specific Todo/Task by ID
- **PATCH** `/todo/{id}` - Update a specific Todo/Task by ID
- **DELETE** `/todo/{id}` - Delete a specific Todo/Task by ID

### Auth

- **POST** `/auth/register` - Register a new user
- **POST** `/auth/login` - Login with user email and password

## Live Swagger API

You can access the live Swagger API documentation at: [https://nestjs-todo-rest-app-tsoc24.vercel.app/swagger](https://nestjs-todo-rest-app-tsoc24.vercel.app/swagger)

![Swagger-UI](https://github.com/user-attachments/assets/b3a54c8c-b4ef-49c8-bdcb-c551ab1577b2)


## Tech Stack

- **NestJS** - A progressive Node.js framework for building efficient, reliable, and scalable server-side applications.
- **Prisma** - An open-source ORM for Node.js and TypeScript that helps manage database schemas and migrations.
- **PostgreSQL** - A powerful, open-source object-relational database system.
- **Swagger** - A tool for designing, building, documenting, and consuming RESTful web services.
- **TypeScript** - A strongly typed programming language that builds on JavaScript.
- **ThunderClient & Postman** - Tools for testing and developing APIs.

## Installation & Setup

### Prerequisites

Before you begin, ensure you have the following installed:

- [Node.js](https://nodejs.org/)
- [pnpm](https://pnpm.io/)
- [PostgreSQL](https://www.postgresql.org/)

### Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/harmeetsingh11/nestjs-todo-rest-app-tsoc24.git
   cd nestjs-todo-rest-app-tsoc24
   ```

2. **Install Dependencies**

   Using pnpm:

   ```bash
   pnpm install
   ```

3. **Set Up Environment Variables**

   - Create a `.env` file in the root directory.
   - Add the following environment variables to the `.env` file. Replace `<YOUR PGADMIN PASSWORD>` with your local pgAdmin password and `<YOUR DATABASE NAME>` with your desired database name. Use any string for the JWT secret.

     ```
     DATABASE_URL="postgresql://postgres:<YOUR PGADMIN PASSWORD>@localhost:5432/<YOUR DATABASE NAME>?schema=public"
     JWT_SECRET="<YOUR JWT SECRET>"
     ```

     **Example `.env` file:**

     ```
     DATABASE_URL="postgresql://postgres:mysecretpassword@localhost:5432/mydatabase?schema=public"
     JWT_SECRET="mysecretjwt"
     ```

4. **Run Database Migrations**

   Using Prisma to push your database schema:

   ```bash
   pnpx prisma migrate dev --name init
   ```

## Running the Application

1. **Start the Development Server**

   Using pnpm:

   ```bash
   pnpm run start:dev
   ```

2. **Access the Application**

   - The application should be running on [http://localhost:3000](http://localhost:3000)
   - Swagger documentation is accessible at [http://localhost:3000/swagger](http://localhost:3000/swagger)

## Testing the API

You can test the API endpoints using tools like `ThunderClient` or `Postman`. 
