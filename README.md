Flutter Responsive Login UI with Bloc

A responsive Flutter authentication UI built using the Bloc pattern from flutter_bloc, demonstrating event-driven state management, transitions, observers, and clean separation of UI and business logic.

🚀 Project Overview

This project showcases a complete authentication flow using Bloc, not Cubit. It includes login, logout, loading states, error handling, navigation based on state changes, and global Bloc observation.

The goal is to demonstrate why and how Bloc is used in real world applications where logic complexity grows beyond simple state updates.

🧠 Why Bloc Instead of Cubit
Bloc is used here intentionally because:
Authentication is event-driven
Multiple states exist for a single feature
Side effects like navigation and SnackBars depend on the state
Transitions need to be tracked and debugged
Scalability and maintainability matter
Cubit would oversimplify this flow and hide important transitions.

🔄 Authentication Flow
User submits login credentials
AuthLoginRequested event is dispatched
Bloc emits AuthLoading
Validation and async logic are executed
Bloc emits AuthSuccess or AuthFailure
UI reacts using BlocConsumer
Navigation occurs based on the state
Logout follows the same event-based lifecycle.

🧩 Key Bloc Concepts Used
BlocProvider for dependency injection
BlocConsumer for UI rendering and side effects
Custom AuthEvent and AuthState classes
Event handlers with on<Event>
State transitions with loading, success, and failure
BlocObserver for global logging and debugging

👀 Global Bloc Observer
This project includes a custom AppBlocObserver to track:
Bloc creation
State changes
Transitions
This is critical for debugging large applications and understanding state flow.

📁 Project Structure
lib/
│
├── bloc/
│   ├── auth_bloc.dart
│   ├── auth_event.dart
│   └── auth_state.dart
│
├── widgets/
│   ├── gradient_button.dart
│   ├── login_field.dart
│   └── social_button.dart
│
├── login_screen.dart
├── home_screen.dart
├── pallete.dart
├── app_bloc_observer.dart
└── main.dart

🎨 UI Features
Responsive layout
Gradient-based buttons
Custom input fields
Dark theme support
Social login UI placeholders
UI is intentionally separated from business logic.

📦 Dependencies
flutter_bloc: ^8.1.0
flutter_svg: ^2.0.7

▶️ How to Run
Clone the repository
git clone <your-repo-url>
Get dependencies
flutter pub get
Run the app
flutter run

🧪 Learning Outcomes
Proper usage of Bloc over Cubit
Event driven architecture
Handling async logic in Bloc
Clean UI and logic separation
Debugging with BlocObserver
Navigation controlled by the state

👨‍💻 Author
Muhammad Junaid
Flutter Developer
Think beyond boundaries
