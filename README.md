

# Airline_Reservation_System

### Highlights of Project

The project includes a UI, also known as GUI (Graphical User Interface), which consists of buttons, text fields, and other graphical elements used to interact with the user. The GUI was built using the Java Swing library.

#### Front End

- **Mainframe Creation**
  - Features in the mainframe: Add customer, search customer, add flights, book flight, generate ticket.
  - Menu bar and menu items: Hovering over menu items displays options.
  - Internal frame: Different from a normal frame, related to the mainframe.
  - Virtual desktop screen.
  - JInternalFrame is used instead of a regular frame to keep menu item screens within the main window.

#### Back End

- MySQL Workbench is used for creating the Airline_Reservation_System project database.
- admin, customer, flight, and ticket tables were created.
- GUI was connected with the database.
- Customer, Flight, Admin, and Ticket IDs were Auto Generated.

#### Connection of Front End and Back End

- A bridge (driver) was required to connect the frontend and backend of the project.
- JDBC driver was used to connect Java with MySQL for the project.

### Working of Project

#### Database Table Creation

- **Admin Table:**

  - `CREATE TABLE admin (AdminID INT, FirstName VARCHAR(255), LastName VARCHAR(255), Username VARCHAR(255), Password VARCHAR(255));`

- **Customer Table:**

  - `CREATE TABLE customer (CustomerID INT, FirstName VARCHAR(255), LastName VARCHAR(255), PassportNo VARCHAR(255), NationalID VARCHAR(255), Address TEXT, Gender VARCHAR(50), DOB DATE);`

- **Flight Table:**

  - `CREATE TABLE flight (FlightID INT, FlightName VARCHAR(255), Arrival TIME, Departure TIME, Duration INT, Seats INT, Fare DECIMAL, DOF DATE);`

- **Ticket Table:**
  - `CREATE TABLE ticket (TicketID INT, FlightID INT, CustomerID INT, Arrival VARCHAR(255), Departure VARCHAR(255), FirstName VARCHAR(255), LastName VARCHAR(255), Gender VARCHAR(50), Contact VARCHAR(255));`

#### Frontend Features

- **Login Page:**
  - Users can log in to the system using their credentials.
- **Main Page:**
  - Includes Customers, Flights, Tickets, Admin menus.
- **Add Customer:**
  - Allows adding a new customer to the system.
  - `INSERT INTO customer VALUES (?, ?, ?, ?, ?, ?, ?, ?, ?);`
- **Search Customer:**
  - Enables searching for customers in the system.
  - `SELECT * FROM customer WHERE CustomerID = ?;`
- **Add Flight:**
  - Functionality to add new flights.
  - `INSERT INTO flight VALUES (?, ?, ?, ?, ?, ?, ?, ?);`
- **Book Flight:**
  - Users can book flights.
  - `INSERT INTO ticket VALUES (?, ?, ?, ?, ?, ?, ?, ?, ?);`
- **View Ticket:**
  - Provides the ability to view booked tickets.
  - `SELECT * FROM ticket WHERE TicketID = ?;`
- **Add Admin:**
  - Adds new admin users.
  - `INSERT INTO admin VALUES (?, ?, ?, ?, ?);`
