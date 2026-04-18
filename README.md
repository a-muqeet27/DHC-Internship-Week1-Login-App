# Flutter Login App

A clean, production-grade Flutter application demonstrating core Flutter concepts: UI building, form validation, and screen navigation.

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

## Tech Stack

- **Framework**: Flutter 3.x
- **Language**: Dart 3.x
- **State Management**: `setState` (built-in, sufficient for this scope)
- **Architecture**: Simple widget-based, screens in `lib/screens/`

---
