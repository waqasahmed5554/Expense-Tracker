# Expense-Tracker
[Download Project](https://drive.google.com/file/d/1rTdnh2mvyHraBkrIqxoj2swuHVU5yCw2/view?usp=sharing)
# 💸 Expense Tracker - Flutter App

![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-3.x-0175C2?style=for-the-badge&logo=dart&logoColor=white)
![Provider](https://img.shields.io/badge/Provider-6.1.2-7B52AB?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Android%20%7C%20iOS-lightgrey?style=for-the-badge)

> A clean, modern **Flutter** personal finance app to track daily income and expenses — featuring a gradient dashboard, category-based filtering, visual reports with charts, user profile management, and multi-platform support.

---

## 📌 Overview

Expense Tracker helps users take full control of their personal finances. Log income and expenses by category, visualize spending patterns through charts, view filtered transaction histories, and manage your profile — all wrapped in a polished, gradient UI built with Flutter and powered by the Provider state management pattern.

---

## 📸 Screenshots

### 🏠 Dashboard
<p align="center">
  <img src="screenshots/dashboard.png" alt="Dashboard Screen" width="300"/>
</p>

### 🔐 Login & Sign Up
<p align="center">
  <img src="screenshots/login.png" alt="Login Screen" width="300"/>
  &nbsp;&nbsp;
  <img src="screenshots/signup.png" alt="Sign Up Screen" width="300"/>
</p>

### 💳 Transactions & Add Expense
<p align="center">
  <img src="screenshots/transactions.png" alt="Transactions Screen" width="300"/>
  &nbsp;&nbsp;
  <img src="screenshots/add_expense.png" alt="Add Expense Screen" width="300"/>
</p>

### 📊 Reports & Settings
<p align="center">
  <img src="screenshots/reports.png" alt="Reports Screen" width="300"/>
  &nbsp;&nbsp;
  <img src="screenshots/settings.png" alt="Settings Screen" width="300"/>
</p>

> 📁 Add your screenshots to the `screenshots/` folder and they will appear here automatically.

---

## ✨ Features

- 🔐 **Authentication Flow** — Login, Sign Up, and Forgot Password screens with form validation
- 🏠 **Dashboard** — Gradient balance card showing Total Balance, Income, and Expenses at a glance
- ➕ **Add Expense / Income** — Form with category picker, payment method selector, date picker, and validation
- 💳 **Transactions Screen** — Filterable list (All / Income / Expense) with categorized transaction tiles
- 📊 **Reports Screen** — Summary cards + `fl_chart` powered pie/bar charts broken down by category
- 👤 **User Profile** — Editable profile with name, email, bio, gender, date of birth, and profile photo picker
- ⚙️ **Settings Screen** — Dark mode toggle, currency selector (PKR), data reset, and logout
- 🧭 **Bottom Navigation** — Smooth tab navigation across Dashboard, Transactions, Reports, and Settings
- 🎨 **Custom Color System** — Centralized `AppColors` with deep navy (`#0A3D62`) and teal (`#38ADA9`) theme

---

## 🖥️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Framework** | Flutter 3.x |
| **Language** | Dart 3.x |
| **State Management** | Provider 6.1.2 |
| **Charts** | fl_chart 0.45 |
| **Image Picker** | image_picker 0.8.7 |
| **Date Formatting** | intl 0.18 |
| **Local Storage** | Hive + Hive Flutter |
| **Unique IDs** | uuid 3.0 |
| **Platform** | Android, iOS, Web, Linux, macOS, Windows |

---

## 📁 Project Structure

```
expense_tracker/
├── lib/
│   ├── main.dart                          # App entry point, MultiProvider setup
│   │
│   ├── models/
│   │   ├── expense_model.dart             # Expense data model (id, title, amount, category, date, isIncome)
│   │   └── user_model.dart                # User data model (name, email, gender, dob, bio, profileImagePath)
│   │
│   ├── providers/
│   │   ├── expense_provider.dart          # Expense state: add, remove, totalIncome, totalExpense, balance
│   │   └── user_provider.dart             # User state: profile info management
│   │
│   ├── screens/
│   │   ├── splash_screen.dart             # Animated splash screen
│   │   ├── auth/
│   │   │   ├── login_screen.dart          # Login with email/password + validation
│   │   │   ├── signup_screen.dart         # New user registration
│   │   │   └── forgot_password_screen.dart # Password recovery
│   │   ├── bottom_nav/
│   │   │   └── bottom_nav_screen.dart     # Bottom navigation bar controller
│   │   ├── Dashboard/
│   │   │   └── dashboard_screen.dart      # Balance card + quick actions + recent transactions
│   │   ├── expenses/
│   │   │   └── add_expense_screen.dart    # Add expense/income form
│   │   ├── transacton/
│   │   │   └── transactions_screen.dart   # Filtered transaction list
│   │   ├── report/
│   │   │   └── reports_screen.dart        # Summary cards + fl_chart charts
│   │   ├── reports_chart/
│   │   │   └── reports_screen.dart        # Extended chart views
│   │   ├── profile/
│   │   │   └── user_profile.dart          # Editable user profile with image picker
│   │   └── settings/
│   │       └── settings_screen.dart       # App preferences and account options
│   │
│   └── utils/
│       └── app_colors.dart                # Global color constants
│
├── android/                               # Android platform files
├── ios/                                   # iOS platform files
├── web/                                   # Web platform files
├── pubspec.yaml                           # Dependencies & project config
└── screenshots/                           # ← Add your screenshots here
```

---

## 🚀 Getting Started

### Prerequisites

- [Flutter SDK](https://docs.flutter.dev/get-started/install) >= 3.7.0
- Dart SDK >= 3.0
- Android Studio / VS Code with Flutter plugin
- Android Emulator or a physical device

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/waqasahmed5554/expense_tracker.git
   cd expense_tracker
   ```

2. **Install dependencies:**
   ```bash
   flutter pub get
   ```

3. **Run the app:**
   ```bash
   # Android / iOS
   flutter run

   # Specific device
   flutter run -d android
   flutter run -d ios

   # Web
   flutter run -d chrome
   ```

4. **Build release APK:**
   ```bash
   flutter build apk --release
   ```

---

## 📦 Dependencies

```yaml
dependencies:
  flutter:
    sdk: flutter
  provider: ^6.1.2           # State management
  fl_chart: ^0.45.1          # Charts & graphs
  image_picker: ^0.8.7+5     # Profile photo selection
  intl: ^0.18.1              # Date & number formatting
  hive: ^2.2.3               # Local key-value storage
  hive_flutter: ^1.1.0       # Hive Flutter integration
  path_provider: ^2.1.0      # File system paths
  uuid: ^3.0.7               # Unique ID generation
  syncfusion_flutter_charts: ^22.2.10+1  # Extended charting
  cupertino_icons: ^1.0.8    # iOS-style icons
```

---

## 🎨 Color Theme

| Name | Color | Hex |
|------|-------|-----|
| Primary | ![#0A3D62](https://placehold.co/15x15/0A3D62/0A3D62.png) Deep Navy | `#0A3D62` |
| Secondary | ![#38ADA9](https://placehold.co/15x15/38ADA9/38ADA9.png) Teal | `#38ADA9` |
| Income | Green Accent | `Colors.green` |
| Expense | Red Accent | `Colors.redAccent` |

---

## 📱 Screens at a Glance

| Screen | Description |
|--------|-------------|
| **Splash** | Animated launch screen |
| **Login** | Email/password login with gradient background |
| **Sign Up** | New account registration |
| **Forgot Password** | Password recovery flow |
| **Dashboard** | Balance card, income/expense summary, quick actions, recent transactions |
| **Add Expense** | Category, amount, payment method, date picker form |
| **Transactions** | All/Income/Expense filtered list with category icons |
| **Reports** | Income, expense, balance summary cards + category pie chart |
| **User Profile** | Editable name, email, bio, gender, DOB, profile photo |
| **Settings** | Dark mode, currency selector, data reset, logout |

---

## 🏗️ Architecture

The app follows a clean **Provider** pattern:

```
UI (Screens/Widgets)
       ↕
  Providers (State)
       ↕
    Models (Data)
```

- `ExpenseProvider` manages the expense list and computes `totalIncome`, `totalExpense`, and `balance`
- `UserProvider` handles user profile state
- All screens consume state via `Provider.of<T>(context)` or `Consumer<T>` widgets

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m 'Add: your feature description'`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a Pull Request

---

---

## 👨‍💻 Developer

**Waqas Ahmed** - AI Developer & Flutter Developer

[![GitHub](https://img.shields.io/badge/GitHub-waqasahmed5554-181717?style=flat&logo=github)](https://github.com/waqasahmed5554)
[![Email](https://img.shields.io/badge/Email-waqasahmed.rk@gmail.com-D14836?style=flat&logo=gmail&logoColor=white)](mailto:waqasahmed.rk@gmail.com)

---

<p align="center">Built with ❤️ using Flutter · Sargodha, Pakistan 🇵🇰</p>
