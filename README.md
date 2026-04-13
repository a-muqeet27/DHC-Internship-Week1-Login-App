# Flutter Login App

A clean, production-grade Flutter application demonstrating core Flutter concepts: UI building, form validation, and screen navigation.

---

## Screenshots

| Login Screen | Validation Errors | Home Screen |
|---|---|---|
| Email + password fields, decorative background | Inline error messages | Dashboard with greeting card & stats |

---

## Features

- ✅ **Login Screen** — email & password `TextFormField`s with icons
- ✅ **Form Validation** — email format check + non-empty password
- ✅ **Navigation** — `Navigator.push()` with a custom fade+slide transition
- ✅ **Home/Dashboard Screen** — greeting card, stats grid, activity feed
- ✅ **Loading State** — spinner during simulated network call
- ✅ **Forgot Password** — `SnackBar` feedback
- ✅ **Animations** — fade + slide entrance on both screens

---

## Project Structure

```
flutter_login_app/
├── lib/
│   ├── main.dart               # App entry point & global theme
│   └── screens/
│       ├── login_screen.dart   # Login UI + validation logic
│       └── home_screen.dart    # Dashboard after successful login
├── test/
│   └── widget_test.dart        # Widget tests for login screen
├── pubspec.yaml
└── README.md
```

---

## Getting Started

### Prerequisites

| Tool | Version |
|---|---|
| Flutter SDK | ≥ 3.10.0 |
| Dart SDK | ≥ 3.0.0 |
| Android Studio / VS Code | Latest |

### 1. Install Flutter

Follow the official guide: https://docs.flutter.dev/get-started/install

Verify installation:
```bash
flutter doctor
```

### 2. Clone & Run

```bash
# Clone the repo
git clone https://github.com/<your-username>/flutter_login_app.git
cd flutter_login_app

# Install dependencies
flutter pub get

# Run on connected device or emulator
flutter run
```

### 3. Run Tests

```bash
flutter test
```

---

## Key Concepts Demonstrated

### Form Validation (`lib/screens/login_screen.dart`)

```dart
String? _validateEmail(String? value) {
  if (value == null || value.trim().isEmpty) return 'Email is required';
  final emailRegex = RegExp(r'^[a-zA-Z0-9._%+\-]+@[a-zA-Z0-9.\-]+\.[a-zA-Z]{2,}$');
  if (!emailRegex.hasMatch(value.trim())) return 'Please enter a valid email address';
  return null;
}
```

### Navigation with Custom Transition

```dart
Navigator.push(
  context,
  PageRouteBuilder(
    pageBuilder: (_, animation, __) => HomeScreen(email: email),
    transitionsBuilder: (_, animation, __, child) =>
        FadeTransition(opacity: animation, child: child),
    transitionDuration: const Duration(milliseconds: 500),
  ),
);
```

---

## Tech Stack

- **Framework**: Flutter 3.x
- **Language**: Dart 3.x
- **State Management**: `setState` (built-in, sufficient for this scope)
- **Architecture**: Simple widget-based, screens in `lib/screens/`

---

## License

MIT © 2024
