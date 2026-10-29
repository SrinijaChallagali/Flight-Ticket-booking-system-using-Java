# Flight Ticket Booking System (Java)

A menu-driven console application for registering users, adding flights, searching routes and booking tickets, written in core Java.

## Features

- **User registration and login** with email and password
- **Add flights** with origin, destination, departure and return dates, airline and price
- **Search flights** by origin, destination and travel dates
- **Sort results by price** using a hand-written quicksort
- **Book a flight** by entering passenger name, date of birth and passport number

## Design

| Class | Responsibility |
|---|---|
| `Flight` | Flight details (route, dates, airline, price) |
| `User` | Registered user account |
| `Booking` | A passenger's booking for a flight |
| `FlightBookingSystem` | Menus, search, quicksort and booking logic |

Data is held in in-memory arrays (up to 100 users, flights and bookings), so it resets each time the program starts.

## How to run

Requires Java 8 or later.

```bash
javac -d out src/flight/FlightBookingSystem.java
java -cp out flight.FlightBookingSystem
```

## Sample session

```
1. Register  2. Login  3. Add Flight  4. Exit
> 3   (add Indigo DEL -> BOM, 5000)
> 3   (add Air India DEL -> BOM, 4200)
> 1   (register)
> 2   (login) -> 1. Search and Sort Flights

Search Results (sorted by price):
Flight ID: 2, Airline: Air India, Origin: DEL, Destination: BOM, ... Price: $4200.0
Flight ID: 1, Airline: Indigo, Origin: DEL, Destination: BOM, ... Price: $5000.0
```

## Possible improvements

- Save users, flights and bookings to files or a MySQL database so data persists between runs
- Make class fields private with getters and setters
- Add an admin role so only admins can add flights
- Store hashed passwords instead of plain text
