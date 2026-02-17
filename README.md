# C++ Railway Seat Reservation System

A simple yet functional command-line based railway seat reservation system built with C++. This application allows users to manage train seat bookings with features to book seats, cancel reservations, and view seat availability.

## Project Overview

This is a mini-project for railway seat management developed using C++ with file persistence capabilities. The system maintains a database of 50 seats and stores reservation data in a text file for data persistence.

## Features

- **Book Seat**: Reserve a specific seat by providing seat number and passenger name
- **Cancel Seat**: Cancel an existing reservation and free up the seat
- **Display Seats**: View the current status of all 50 seats
- **Data Persistence**: All bookings are automatically saved to a file (`railway_data.txt`)
- **Error Handling**: Comprehensive exception handling for invalid operations

## System Requirements

- C++ compiler (C++11 or later)
- Standard C++ libraries (iostream, fstream, string, stdexcept)
- macOS, Linux, or Windows with a C++ development environment

## Installation & Setup

1. **Clone the Repository** (if using Git):
   ```bash
   git clone https://github.com/Yuvrajmishra-cell/C---MINI-PROJECT.git
   cd "cpp mini project"
   ```

2. **Compile the Program**:
   ```bash
   g++ -o railway_system project.cpp
   ```
   or
   ```bash
   clang++ -o railway_system project.cpp
   ```

3. **Run the Program**:
   ```bash
   ./railway_system
   ```

## Usage

Once the program is running, you'll see an interactive menu:

```
=== Railway Reservation System ===
1. Book Seat
2. Cancel Seat
3. Display Seats
4. Exit
```

### Booking a Seat

1. Select option `1` from the menu
2. Enter the seat number (1-50)
3. Enter the passenger name
4. The system will confirm the booking or display an error if the seat is unavailable

### Canceling a Seat

1. Select option `2` from the menu
2. Enter the seat number to cancel
3. The system will free up the seat and update the records

### Viewing All Seats

1. Select option `3` to display the status of all 50 seats
2. Each seat will show either "Available" or the passenger's name

### Exit

1. Select option `4` to exit the application

## Technical Details

### Architecture

The program uses an Object-Oriented approach with a main `Railway` class that handles:
- Seat management (array of 50 seats)
- File I/O operations (loading and saving data)
- Business logic for booking and cancellation

### Data Storage

- **File Name**: `railway_data.txt`
- **Format**: One seat status per line (50 lines total)
- **Content**: Either "Available" or passenger name for each seat

### Key Methods

| Method | Description |
|--------|-------------|
| `bookSeat(int seatNum, string name)` | Books a specific seat for a passenger |
| `cancelSeat(int seatNum)` | Cancels a booking and frees up the seat |
| `displaySeats()` | Displays all seat statuses |
| `saveToFile()` | Persists seat data to `railway_data.txt` |
| `loadFromFile()` | Loads seat data from `railway_data.txt` at startup |

### Exception Handling

The system implements robust error handling:
- `out_of_range`: Thrown when seat number is outside valid range (1-50)
- `runtime_error`: Thrown for invalid operations (booking already booked seat, canceling empty seat, file I/O errors)

## Data Persistence

The application automatically saves all changes to `railway_data.txt`. When the program starts, it loads the previous state of reservations from this file, ensuring data persistence across sessions.

## Limitations & Future Enhancements

### Current Limitations
- Single thread - does not handle concurrent bookings
- Basic text-based interface
- No password protection or user authentication
- Limited to 50 seats (hardcoded constant)

### Possible Future Improvements
- Multi-threading support for concurrent bookings
- Graphical User Interface (GUI)
- Database integration (SQL)
- User authentication and role-based access
- Train information (routes, schedules, pricing)
- Payment processing
- Seat selection visualization
- Email/SMS confirmation notifications

## Files in This Project

- `project.cpp` - Main source code file
- `C++ Railway Seat Reservation System.pdf` - Project specifications and requirements
- `documentation.pdf` - Detailed documentation
- `railway_data.txt` - Data file (auto-generated on first run)
- `README.md` - This file

## Compilation Options

### Debug Mode (with debugging symbols)
```bash
g++ -g -o railway_system project.cpp
```

### Optimized Build
```bash
g++ -O2 -o railway_system project.cpp
```

## Troubleshooting

| Issue | Solution |
|-------|----------|
| File permission error | Ensure write permissions in the directory |
| Compilation errors | Verify C++ compiler is installed and in PATH |
| Data not persisting | Check if `railway_data.txt` can be written |
| Invalid input | Make sure to enter valid seat numbers (1-50) and valid names |

## Author

**Yuvraj Mishra**
- GitHub: [@Yuvrajmishra-cell](https://github.com/Yuvrajmishra-cell)
- Repository: [C---MINI-PROJECT](https://github.com/Yuvrajmishra-cell/C---MINI-PROJECT)

## License

This project is part of an academic assignment.

## Acknowledgments

- Based on C++ mini-project requirements for railway management systems
- Standard Library documentation and best practices

---

**Last Updated**: February 17, 2026
