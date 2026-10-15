# 📱 MAD Practical 5 — Login & Registration UI (Jetpack Compose)

![Platform](https://img.shields.io/badge/Platform-Android-3DDC84?logo=android&logoColor=white)
![Language](https://img.shields.io/badge/Language-Kotlin-7F52FF?logo=kotlin&logoColor=white)
![UI](https://img.shields.io/badge/UI-Jetpack%20Compose-4285F4?logo=jetpackcompose&logoColor=white)
![Min SDK](https://img.shields.io/badge/minSdk-26-blue)
![Target SDK](https://img.shields.io/badge/targetSdk-37-blue)

**Subject:** Mobile Application Development (MAD)
**Enrollment No.:** 25172022054
**Practical No.:** 5

---

## 📖 Overview

An Android app built entirely with **Jetpack Compose** that demonstrates a **Login screen** and a **Registration screen** connected through **Navigation Compose**. A reusable `FormField` composable is shared by both screens, and basic input validation is shown to the user through Toast messages.

## 🎯 Aim

To design and develop a login and registration user interface using Jetpack Compose, with screen navigation, reusable composables, state handling and form validation.

## ✨ Features

- 🔐 **Login screen** with Email and Password fields, a "Forgot Password?" link and a Login button
- 📝 **Registration screen** with Name, Phone Number, City, Email, Password and Confirm Password
- 🔁 **Navigation** between screens (`login` ⇄ `register`) using `NavHost` and `NavController`
- ♻️ **Reusable `FormField` composable** (label + outlined text field in one row)
- 🙈 Password fields are masked using `PasswordVisualTransformation`
- ⌨️ Smart keyboard types: phone → numeric/phone, email → email keyboard
- 🔢 Phone field accepts **digits only**
- ✅ **Validation** with Toast feedback:
  - Login: email and password must not be empty
  - Register: all fields required, passwords must match, phone number must be at least 10 digits
- 🎨 Card-based layout with rounded corners, elevation and the GUNI logo
- 👀 `@Preview` functions for quick design checks in Android Studio

## 🧭 App Flow

```
        ┌──────────────┐   SIGN UP    ┌──────────────────┐
        │ Login Screen │ ───────────► │ Register Screen  │
        │  (start)     │ ◄─────────── │                  │
        └──────────────┘ LOGIN / done └──────────────────┘
```

## 🛠️ Tech Stack

| Component | Details |
|---|---|
| Language | Kotlin |
| UI Toolkit | Jetpack Compose (Material 3) |
| Navigation | Navigation Compose |
| Build System | Gradle (Kotlin DSL) with version catalog |
| Min SDK | 26 (Android 8.0) |
| Target SDK | 37 |
| IDE | Android Studio |

## 📂 Project Structure

```
25172022054_mad_practical5/
├── app/
│   └── src/main/
│       ├── java/com/new_app/a25172022054_mad_practical5/
│       │   ├── MainActivity.kt        # Entry point + NavHost (login / register routes)
│       │   ├── LoginForm.kt           # LoginActivityUI composable
│       │   ├── RegistrationForm.kt    # RegisterUI composable + validation
│       │   ├── FormField.kt           # Reusable labelled input field
│       │   └── theme/                 # Color.kt, Type.kt, Theme.kt
│       ├── res/
│       │   ├── drawable/              # guni_pink_logo.png, launcher icons
│       │   ├── values/                # strings, colors, themes
│       │   └── xml/                   # backup / data extraction rules
│       └── AndroidManifest.xml
├── gradle/                            # Wrapper + libs.versions.toml
├── build.gradle.kts
└── settings.gradle.kts
```

## 🚀 Getting Started

### Prerequisites
- Android Studio (latest stable recommended)
- JDK 17 or above
- An Android emulator or a physical device running Android 8.0 (API 26) or higher

### Run the project

```bash
# 1. Clone the repository
git clone https://github.com/Prince-Prajapati-Maheshbhai/25172022054_mad_practical5.git

# 2. Open the folder in Android Studio and let Gradle sync

# 3. Select an emulator / device and click ▶ Run
```

Or build from the terminal:

```bash
./gradlew assembleDebug        # Linux / macOS
gradlew.bat assembleDebug      # Windows
```

## 📚 Concepts Covered

- Composable functions and state (`remember`, `mutableStateOf`)
- State hoisting for reusable components
- `OutlinedTextField`, `Card`, `Button`, `Scaffold`
- `KeyboardOptions` and `VisualTransformation`
- Navigation Compose (`NavHost`, `composable`, `popBackStack`)
- Toast messages from Compose via callbacks

## 👤 Author

**Prince Prajapati**

Enrollment No.: 25172022054
