# Droovo Mobile App (Public)

Welcome to the **public Droovo Flutter app repository**! This repo contains only a subset of the Flutter app: helper classes and testable code that external contributors can work on and improve.

> ⚠️ **Note:** Sensitive code and the full app are maintained in the private Droovo GitLab repository.

---

## Table of Contents

* [Project Overview](#project-overview)
* [Getting Started](#getting-started)
* [Contributing](#contributing)
* [CI/CD & Testing](#cicd--testing)
* [Workflow for Updates](#workflow-for-updates)
* [Reporting Issues](#reporting-issues)
* [License](#license)

---

## Project Overview

This public repository contains:

* `helpers/` directory: utility classes and shared code safe for public contribution.
* `main_public.dart`: a lightweight, testable app entry point for contributors.
* Unit tests for helper classes.

The full app, including sensitive business logic, payment, and backend integrations, is in the private GitLab repository.

---

## Getting Started

### Prerequisites

* [Flutter](https://flutter.dev/docs/get-started/install) ≥ 3.x
* Android Studio / Xcode (for device builds)
* Git

### Clone the repository

```bash
git clone https://github.com/droovo/droovo-mobile-public.git
cd droovo-mobile-public
```

### Install dependencies

```bash
flutter pub get
```

### Run the testable app

```bash
flutter run -t lib/main_public.dart
```

This launches the app with the public helper code, allowing you to test changes safely.

---

## Contributing

We welcome contributions! Please follow these guidelines:

1. **Fork the repository**.
2. **Create a feature branch** for your changes:

```bash
git checkout -b contrib/my-feature
```

3. **Modify or add helper classes** only. Do not attempt to access sensitive or private logic.
4. **Run tests locally**:

```bash
flutter test
```

5. **Submit a pull request (PR)** to the `contrib/*` branch. GitHub Actions will automatically run tests.

---

## CI/CD & Testing

* All PRs trigger automated Flutter tests and code analysis.
* Only helper classes and `main_public.dart` are tested.
* Builds are optional for Android and iOS testing.

---

## Workflow for Updates

1. Contributors submit PRs to the public repo.
2. After review and testing, approved changes to helper classes are manually merged into the private GitLab repository.
3. `main_public.dart` is for testing purposes and **is not merged** into the private repo.

This workflow ensures contributors can safely improve shared code without exposing the full app.

---

## Reporting Issues

* Submit an issue if you find bugs or have improvement suggestions.
* Provide a detailed description, steps to reproduce, and screenshots if possible.

---

## License

This project is maintained by **Droovo**. Contributions are governed by the terms in the [LICENSE](LICENSE) file.

---

Thank you for helping make Droovo better! 🚀
