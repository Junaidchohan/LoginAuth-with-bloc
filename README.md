##Flutter Responsive Login UI with Bloc

A responsive Flutter authentication UI built using the Bloc pattern from flutter_bloc.
This project demonstrates event driven state management, state transitions, BlocObserver, and a clean separation of UI and business logic.

#🚀 Project Overview
This project implements a complete authentication flow using Bloc, not Cubit.
It includes:
Login and logout flow
Loading, success, and failure states
Error handling with SnackBars
Navigation based on state changes
Global Bloc observation for debugging
This repository exists to show when Bloc is the correct choice as application logic grows in complexity.

🧠 Why Bloc Instead of Cubit
Bloc is used intentionally because:
Authentication is event driven
A single feature has multiple possible states
Navigation and UI side effects depend on state
Transitions must be observable and debuggable
Scalability and long term maintainability matter
Cubit would oversimplify this flow and hide important transitions.

🔄 Authentication Flow
User submits login credentials
AuthLoginRequested event is dispatched
Bloc emits AuthLoading
Validation and async logic execute
Bloc emits AuthSuccess or AuthFailure
UI reacts using BlocConsumer
Navigation occurs based on emitted state
Logout follows the same event based lifecycle.

🧩 Bloc Concepts Demonstrated
BlocProvider for dependency injection
BlocConsumer for UI rendering and side effects
Custom AuthEvent and AuthState
Event handlers using on<Event>
Loading, success, and failure state transitions
BlocObserver for global logging

👀 Global Bloc Observer
A custom AppBlocObserver is implemented to track:
Bloc creation
State changes
State transitions
This is essential for debugging and monitoring large scale applications.

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

````🎨 UI Features
Responsive layout
Gradient based buttons
Custom input fields
Dark theme
Social login UI placeholers
UI remains fully separated from business logic.

📦 Dependencies
flutter_bloc: ^8.1.0
flutter_svg: ^2.0.7

▶️ How to Run
1. Clone the repository
git clone <your-repo-url>
2. Install depndencies
flutter pub get
3. Run the application
flutter run

🧪 Learning Outcomes
Correct usage of Bloc over Cubit
Event driven architecture
Async logic handling inside Bloc
UI and logic separation
Debugging using BlocObserver
State controlled navigation

📈 Future Improvements
Replace mock authentication with Firebase
Add form validation Bloc
Implement signup and forgot password flows
Persist auth state using HydratedBloc
Add unit tests and Bloc tests

👨‍💻 Author
Muhammad Junaid
Flutter Developer
Think beyond boundaries
