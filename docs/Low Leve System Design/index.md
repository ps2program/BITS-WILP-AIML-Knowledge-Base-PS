# Low Level Design Patterns

Here's a list of some top low-level design patterns, which are often used to handle more specific, implementation-level concerns in software development. These patterns are generally more focused on solving particular, frequently occurring coding problems:

### 1. **Factory Method**
   - **Purpose:** Provides an interface for creating objects in a superclass but allows subclasses to alter the type of objects that will be created.
   - **Example Use Case:** When a class can't anticipate the class of objects it needs to create.

### 2. **Singleton**
   - **Purpose:** Ensures that a class has only one instance and provides a global point of access to it.
   - **Example Use Case:** Managing resources such as database connections, logging, or configuration settings.

### 3. **Adapter**
   - **Purpose:** Allows incompatible interfaces to work together by wrapping an incompatible class with a compatible interface.
   - **Example Use Case:** Integrating third-party libraries into your codebase without modifying the original code.

### 4. **Decorator**
   - **Purpose:** Adds new functionality to an object dynamically without altering its structure.
   - **Example Use Case:** Extending functionalities like logging, authentication, or validation on a per-object basis.

### 5. **Proxy**
   - **Purpose:** Provides a placeholder for another object to control access, manage resources, or add functionality.
   - **Example Use Case:** Implementing lazy loading, access control, or logging for objects that are expensive to create.

### 6. **Observer**
   - **Purpose:** Establishes a one-to-many dependency between objects so that when one object changes state, all dependents are notified and updated automatically.
   - **Example Use Case:** Implementing event handling systems, such as notifying subscribers of changes in real-time applications.

### 7. **Strategy**
   - **Purpose:** Defines a family of algorithms, encapsulates each one, and makes them interchangeable to let clients choose the behavior at runtime.
   - **Example Use Case:** Selecting algorithms based on context, such as different sorting strategies or encryption algorithms.

### 8. **Command**
   - **Purpose:** Encapsulates a request as an object, allowing for parameterization of clients with queues, logging, or undoable operations.
   - **Example Use Case:** Creating a sequence of actions, such as implementing an undo-redo mechanism.

### 9. **Chain of Responsibility**
   - **Purpose:** Passes requests along a chain of handlers, where each handler decides to process the request or pass it along.
   - **Example Use Case:** Handling authentication, logging, or request validation.

### 10. **Template Method**
   - **Purpose:** Defines the skeleton of an algorithm, letting subclasses redefine certain steps without altering the structure.
   - **Example Use Case:** Implementing a sequence of steps with common structure but specific details.

### 11. **Builder**
   - **Purpose:** Constructs complex objects step-by-step, allowing customization and reuse of the construction process.
   - **Example Use Case:** Constructing objects with multiple configurations or optional parameters, such as configuring a complex UI component.

### 12. **Prototype**
   - **Purpose:** Creates new objects by copying an existing object, rather than creating them from scratch.
   - **Example Use Case:** Duplicating objects where creating a new instance is resource-intensive.

### 13. **State**
   - **Purpose:** Allows an object to alter its behavior when its internal state changes.
   - **Example Use Case:** Implementing a finite-state machine where the object’s behavior varies according to its state, such as state transitions in UI components.

### 14. **Flyweight**
   - **Purpose:** Shares common parts of objects to reduce memory usage, especially when dealing with a large number of similar objects.
   - **Example Use Case:** Managing a large number of lightweight objects, like rendering a forest of trees in a game, where each tree shares the same structure.

### 15. **Mediator**
   - **Purpose:** Centralizes complex communications and control between related objects to reduce coupling.
   - **Example Use Case:** Implementing chat rooms, where each participant communicates via a central mediator.

These low-level patterns help improve code maintainability, flexibility, and reusability by offering solutions to common challenges in object-oriented design.

# LLD Interview Questions

Here are some popular low-level design interview questions that test your ability to architect and implement efficient solutions for various real-world problems. These questions often focus on specific object-oriented design patterns, data modeling, and detailed class structure implementations.

### 1. **Design a Parking Lot System**
   - **Objective:** Design a system to manage parking spots, vehicles, and ticketing.
   - **Considerations:** Types of parking spots (small, medium, large), vehicle types, parking fees, and managing available spots.
   - **Expected Output:** Class diagram with classes like `ParkingLot`, `ParkingSpot`, `Vehicle`, `Ticket`, and relationships between them.

### 2. **Design an Elevator System**
   - **Objective:** Implement an elevator system for a multi-floor building.
   - **Considerations:** Multiple elevators, button panels (inside and outside), up/down requests, elevator states (moving, idle, maintenance).
   - **Expected Output:** Classes like `Elevator`, `ElevatorController`, `Floor`, `Request`, and methods to handle requests and manage elevator states.

### 3. **Design an ATM System**
   - **Objective:** Design a system for an ATM that dispenses cash and supports balance checks, deposits, and PIN verification.
   - **Considerations:** User authentication, different types of accounts, available denominations, and error handling (e.g., insufficient funds).
   - **Expected Output:** Classes like `ATM`, `Account`, `CardReader`, `Transaction`, `CashDispenser`, and methods for withdrawal, deposit, and balance inquiry.

### 4. **Design an Online Book Reader (eBook System)**
   - **Objective:** Create a system that supports reading books online with features like search, bookmarks, and user accounts.
   - **Considerations:** User library, book storage, bookmarks, recommendations, and search.
   - **Expected Output:** Classes such as `User`, `Book`, `Library`, `Bookmark`, `Reader`, and interactions between them.

### 5. **Design a Movie Ticket Booking System**
   - **Objective:** Build a ticket reservation system for a movie theater.
   - **Considerations:** Seating arrangement, movie schedule, show times, pricing, booking, and cancellation.
   - **Expected Output:** Classes like `Theater`, `Screen`, `Show`, `Seat`, `Ticket`, and methods to reserve and cancel seats.

### 6. **Design a Restaurant Reservation System**
   - **Objective:** Implement a system to handle table reservations for a restaurant.
   - **Considerations:** Table types and availability, reservation slots, user cancellations, and walk-in guests.
   - **Expected Output:** Classes such as `Restaurant`, `Table`, `Reservation`, `User`, and methods to create, modify, and cancel reservations.

### 7. **Design a Library Management System**
   - **Objective:** Create a system for managing books, patrons, and librarians in a library.
   - **Considerations:** Book search, borrowing, returning, overdue fees, and managing users.
   - **Expected Output:** Classes like `Library`, `Book`, `Member`, `Librarian`, `Loan`, and interactions between them.

### 8. **Design a File Storage System (like Dropbox)**
   - **Objective:** Create a simplified file storage service allowing users to upload, download, and organize files.
   - **Considerations:** File versioning, permissions, storage structure, and folder management.
   - **Expected Output:** Classes such as `User`, `File`, `Folder`, `Permission`, and methods for uploading, downloading, and organizing files.

### 9. **Design a Chess Game**
   - **Objective:** Design the data structures for a basic chess game allowing two players to play and manage game rules.
   - **Considerations:** Board setup, piece types, moves, capturing rules, and check/checkmate detection.
   - **Expected Output:** Classes like `Game`, `Board`, `Player`, `Piece` (with subclasses for each piece), and methods to validate moves and track the game state.

### 10. **Design a Social Media News Feed**
   - **Objective:** Implement a system that allows users to post, like, follow others, and see a personalized feed.
   - **Considerations:** Feed generation, friend/follower relationships, post privacy settings, and interactions (likes, comments).
   - **Expected Output:** Classes such as `User`, `Post`, `Comment`, `Like`, `Feed`, and methods for creating, updating, and fetching posts.

### 11. **Design a Notification System**
   - **Objective:** Design a notification system that sends alerts through multiple channels like email, SMS, and push notifications.
   - **Considerations:** Different notification types, user preferences, retry mechanisms, and delivery channels.
   - **Expected Output:** Classes like `Notification`, `User`, `Channel` (subclasses for Email, SMS, Push), and methods for sending and managing notifications.

### 12. **Design a Hotel Booking System**
   - **Objective:** Design a system that allows users to book rooms in a hotel.
   - **Considerations:** Room types, booking slots, pricing, and cancellation policies.
   - **Expected Output:** Classes such as `Hotel`, `Room`, `Booking`, `User`, `Payment`, and methods to book, modify, and cancel bookings.

### 13. **Design a URL Shortener Service**
   - **Objective:** Build a service that shortens long URLs and allows redirection.
   - **Considerations:** URL mapping, expiration dates, analytics tracking, and hash generation.
   - **Expected Output:** Classes like `URLShortener`, `URLMapping`, `User`, and methods to create and resolve shortened URLs.

### 14. **Design a Snake and Ladder Game**
   - **Objective:** Create the classes and interactions for a basic Snake and Ladder game.
   - **Considerations:** Game board, players, snakes, ladders, and dice.
   - **Expected Output:** Classes such as `Game`, `Board`, `Player`, `Snake`, `Ladder`, and methods to handle player moves and determine game status.

### 15. **Design a Ride Sharing System (like Uber)**
   - **Objective:** Implement a system to handle ride requests, driver location, and matching riders with drivers.
   - **Considerations:** Ride requests, driver availability, location tracking, pricing, and trip management.
   - **Expected Output:** Classes like `Rider`, `Driver`, `RideRequest`, `Location`, `Ride`, and methods for requesting and managing rides. 

These questions help assess your understanding of object-oriented principles, data modeling, and the ability to apply design patterns in specific scenarios. Preparing for these will give you strong foundational knowledge for low-level design interviews.