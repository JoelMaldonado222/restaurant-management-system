# Restaurant Management System 🍽️

A full-stack Java desktop application for managing restaurant operations 
employees, menu items, payroll, and more. Built with OOP principles, 
JDBC/SQLite persistence, and a modern dark-themed Swing GUI.


## Tech Stack
- **Language:** Java 17
- **GUI:** Java Swing (custom dark theme, gradient backgrounds, hover animations)
- **Database:** SQLite via JDBC
- **Testing:** JUnit 5 (11 unit tests)
- **Build:** IntelliJ IDEA / Maven

## Features
- ✅ Modern dark-themed GUI with animated hover effects
- ✅ Employee management — add, remove, update, display
- ✅ Menu management — add, remove, update dishes
- ✅ Weekly payroll calculator
- ✅ SQLite database persistence via JDBC
- ✅ File-based data import (CSV)
- ✅ Input validation across all layers
- ✅ Toggle restaurant open/late hours status
- ✅ JUnit 5 test suite covering all core business logic

## Architecture
RestaurantAppGUI.java  → Swing GUI layer (dark theme, animations)
RestaurantApp.java     → CLI interface + controller logic
Restaurant.java        → Core business logic layer
Employee.java          → Employee model with validation
Dish.java              → Dish/menu item model with validation
DatabaseManager.java   → JDBC/SQLite connection & CRUD operations
RestaurantAddTest.java → JUnit 5 test suite

## How to Run
1. Clone the repo
2. Open in IntelliJ IDEA
3. Make sure `sqlite-jdbc` is in your `/libs` folder
4. Run `RestaurantAppGUI.java` for the GUI
5. Or run `RestaurantApp.java` for the CLI version
6. Click "Load Data" and select any `.db` file to connect

## Running Tests
Open `RestaurantAddTest.java` and run with JUnit 5. All 11 tests should pass.

## OOP Design
The system uses a layered architecture:
- **Model layer:** `Employee`, `Dish` — encapsulated data with validation
- **Business layer:** `Restaurant` — manages collections and business rules
- **Data layer:** `DatabaseManager` — handles all JDBC/SQLite operations
- **View layer:** `RestaurantAppGUI` — modern Swing interface
