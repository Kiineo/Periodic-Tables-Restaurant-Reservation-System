# Periodic-Tables-Restaurant-Reservation-System

**Periodic-Tables-Restaurant-Reservation-System** is a full-stack web application developed as a capstone project for Thinkful's Bootcamp Engineering Program. The project aims to create a reservation system for fine dining restaurants, which will be used exclusively by restaurant personnel for handling customer reservations.

## Summary

The capstone project involved building a reservation system for fine dining restaurants. The software allows restaurant personnel to manage reservations efficiently and provides various functionalities such as creating and editing reservations, searching for reservations, adding new tables, seating customers, marking reservations as finished, and canceling reservations.

The project requirements included using React for the client-side, Node.js and Express for the API, and PostgreSQL for the database. The development process followed a test-driven approach, with provided tests serving as a guideline for implementation.

## Deployed Application

The site is deployed using render at this link: https://periodic-tables-restaurant-reservation.onrender.com/dashboard

## Client Descriptions

### Dashboard

The Dashboard page provides an overview of reservations for a specific date. It displays a sorted list of reservations, showing customer names, mobile numbers, reservation times, and party sizes. The dashboard allows restaurant personnel to view and manage reservations for a particular day, facilitating efficient seating arrangements. It also includes navigation buttons to switch between different dates and displays error messages if any issues occur.

### Create a Reservation

The Create a Reservation page allows restaurant personnel to create a new reservation for a customer. It provides a form where users can enter the necessary details, including the customer's first and last name, mobile number, date of the reservation, time of the reservation, and the number of people in the party. After submitting the form, the system saves the reservation and redirects the user to the corresponding date's dashboard page.

### Create a Table

The Create a Table page enables restaurant personnel to add new tables to the seating arrangement. It includes a form where users can enter the table number, capacity (number of seats), and other relevant details. This feature helps in managing available seating options and ensures accurate table assignments for reservations.

### Edit Reservation

The Edit Reservation page allows restaurant personnel to modify the details of an existing reservation. It presents a form pre-populated with the reservation's current information, allowing users to make necessary changes such as updating the customer's name, mobile number, date, time, or party size. After submitting the edited form, the system saves the changes and updates the reservation accordingly.

### Seat Reservation

The Seat Reservation page is used to assign a reserved table to a customer. When a customer arrives for their reservation, the restaurant personnel can use this feature to assign them a table. This action updates the reservation status and the assigned table, ensuring accurate tracking of seating arrangements and preventing double bookings.

### Search

The Search page enables restaurant personnel to search for reservations based on specific criteria. Currently, it is only implemented for searching phone numbers. Users can input their search parameters and retrieve a list of matching reservations. This feature is particularly useful when dealing with a large number of bookings, allowing for quick and efficient reservation retrieval.

## API

The application's API provides the following endpoints:

- `GET /reservations`: Lists all reservations, sorted by time.
- `POST /reservations`: Creates a new reservation.
- `GET /reservations/:reservation_id`: Retrieves a reservation by reservation ID.
- `PUT /reservations/:reservation_id`: Updates a reservation by reservation ID.
- `PUT /reservations/:reservation_id/status`: Updates a reservation's status by reservation ID.
- `GET /reservations?mobile_number=XXXXXXXXXX`: Lists all reservations for a given mobile number, sorted by time.
- `GET /tables`: Lists all tables, sorted by table name.
- `POST /tables`: Creates a new table.
- `PUT /tables/:table_id/seat`: Updates a table and assigns it to a reservation.
- `DELETE /tables/:table_id/seat`: Frees an occupied table by deleting the assigned reservation ID.

## Installation

To install and run the project locally, follow these steps:

1. Fork and clone this repository.
2. Run the following command to copy the `.env.sample` file to `.env` in the back-end directory:
3. Update the `./back-end/.env` file with the connection URLs to your ElephantSQL database instance.
4. Run the following command to copy the `.env.sample` file to `.env` in the front-end directory:
	- You only need to modify the `./front-end/.env` file if you want to connect to a backend at a location other than `http://localhost:5000`.
5. Run the following command to install project dependencies:npm install
6. Run `npm run start:dev` to start the server in development mode.
