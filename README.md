# Simple Bank Client Management System (C++)

A console-based client management system written in C++. It allows you to manage bank client records, store them in a text file, and perform basic CRUD (Create, Read, Update, Delete) operations.

## Features

- Add a new client (with duplicate account number prevention)
- Show all clients in a formatted table
- Find a client by account number and display their details
- Update client information (leave fields empty to keep old values)
- Delete a client (soft delete with confirmation)
- Sort clients in ascending order by account number
- Data is persisted in a text file (`ZDFile.txt`)

## How It Works

The program stores client records in a local text file named `ZDFile.txt`. Each client record is saved as a single line using `#//#` as a field separator. When the program loads, it reads the entire file into memory, performs the requested operations, and writes the updated list back to the file.

The deletion operation uses a "Mark for Delete" technique: instead of removing the record immediately, it flags the client as deleted. When saving, only non-marked records are written to the file.

## File Format
AccountNumber#//#PinCode#//#Name#//#PhoneNumber#//#Balance.

Example:
A150#//#0000#//#AD#//#123456789#//#5270.5
B200#//#1111#//#BD#//#987654321#//#12000.0

## How to Run

1. Clone the repository or download the source files.
2. Open the project in any C++ IDE (e.g., Visual Studio, Code::Blocks, Dev-C++).
3. Compile and run the main source file.
4. The program will display a main menu where you can choose the desired operation.

## Menu Options

- **[1] Show All Clients** – Displays a table of all clients.
- **[2] Add New Client** – Adds a new client (prevents duplicate account numbers).
- **[3] Delete a Client** – Deletes a client by account number (requires confirmation).
- **[4] Update a Client** – Updates client information (press Enter to keep current value).
- **[5] Find a Client** – Searches for a client by account number and shows their details.
- **[0] Exit** – Exits the program.

## Requirements

- A C++ compiler supporting C++11 or later.
- Windows operating system (uses `system("cls")` and `system("pause>0")` for console management). These can be replaced for cross-platform compatibility.

## Project Structure

- `main.cpp` – Contains the entire application logic.
- `ZDFile.txt` – The data file (created automatically when adding clients).

## Learning Outcomes

This project demonstrates proficiency in:
- Procedural programming in C++
- File I/O operations (reading from and writing to text files)
- String manipulation and tokenization
- Vectors and structures for data management
- Sorting algorithms (Bubble Sort)
- Input validation and error handling
- Simple console user interface design

---

**Created as a learning project to master C++ fundamentals.**