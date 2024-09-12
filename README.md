# Hive Mobile App

Welcome to **Hive App**, an innovative mobile application designed to revolutionize how you find and utilize workspaces or study environments. Whether you're searching for a quiet place to work or a comfortable study area, Hive App is here to help you discover the perfect spot with ease.

---
## Project Overview

### Objective

The Hive App aims to solve the common problem of finding suitable workspaces or study environments when traditional coworking spaces are either unavailable or overcrowded. The application connects users with nearby locations that offer comfortable and conducive environments for work or study. Our intelligent recommendation system leverages AI and computer vision to assess and suggest the most appropriate spaces based on real-time data.

---

## Project Structure

This project uses **Clean Architecture** with the following main layers:

![Project Structure](https://github.com/user-attachments/assets/ee2baa54-804a-4654-82ed-078c3eb4a33a)

### Explanation of Layers

- **Common**: Contains shared constants and resources used across different parts of the app.
- **Data Layer**: Manages the app's data. Data is fetched from remote sources (e.g., APIs via Retrofit) or local sources (e.g., Room database). The repository combines these sources to provide data to the domain layer.
- **Domain Layer**: Contains business logic and core models. Use cases encapsulate the app's operations and are consumed by the presentation layer.
- **Presentation Layer**: This layer handles the UI and interaction logic. It includes various screens (e.g., authentication, booking, home), and the ViewModels interact with the domain layer.

```plaintext
hive_mobile/
│
├── common/                   # Shared utilities and constants
│   ├── Constants              # Holds constant values used across the app
│   └── Resource               # Resource management (strings, colors, etc.)
│
├── data/                     # Data sources and repositories
│   ├── local/                # Local data sources (Room, SharedPreferences)
│   ├── remote/               # Remote data sources (APIs, Retrofit services)
│   └── repository/           # Repository for combining local and remote data
│
├── di/                       # Dependency Injection
│   └── AppModule             # Dagger Hilt modules for injecting dependencies
│
├── domain/                   # Business logic and use cases
│   ├── model/                # Domain models representing core entities
│   ├── repository/           # Domain layer repository interfaces
│   └── use_case/             # Business logic (use cases)
│
├── presentation/             # UI layer and ViewModels
│   ├── authentication/       # Screens for login, signup, etc.
│   ├── main_screen/          # Main screens of the app
│   │   ├── booking/          # Booking-related screens
│   │   ├── home/             # Home screen, components, etc.
│   │   │   └── HomeScreen.kt # Kotlin file for home screen UI
│   │   ├── more/             # Additional screens or sections
│   │   └── search/           # Search functionality
│   └── ui/                   # General UI components (buttons, modals, etc.)

```
---
## Key Features

- **Booking System**: Users can browse and book services.
- **Authentication**: Secure login and sign-up system.
- **Home Screen**: Personalized experience with components showing user-relevant data.
- **Search**: Allows users to search for services easily.
- **Clean Architecture**: Structured to scale and maintain easily.

## Technologies Used

- **Kotlin**: Programming language.
- **Jetpack Compose**: Modern toolkit for building native Android UIs.
- **Retrofit**: For handling network requests.
- **Room**: Local database management.
- **Dagger Hilt**: For dependency injection.
- **Coroutines**: For asynchronous programming.
- **Material Design 3**: UI design and components.

## Modules

- **Authentication**: Manages user login and registration.
- **Booking**: Allows users to browse and book services.
- **Home**: Displays personalized content on the home screen.
- **Search**: Enables searching for specific services or items.

Each module follows the Clean Architecture pattern, separating data, domain, and presentation concerns to ensure maintainability and scalability.

---

Thank you for exploring the Hive App! We are excited to help you find the ideal workspace or study environment that meets your needs with cutting-edge technology and a user-centric approach. For further information or inquiries, feel free to reach out to our team members.
