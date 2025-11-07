# 📱 Appium Python Automation Framework

This repository contains a modular and scalable **mobile test automation framework** built using **Appium** and **Python (Pytest)**.
It is designed for end-to-end testing of Android applications, integrating advanced reporting, reusable utilities, and configurable fixtures.

---

## 🧩 Project Structure

```
appium-python-automation/
├── .venv/                  # Virtual environment for Python dependencies
├── allure-report/           # Generated Allure test reports
├── fixtures/                # Pytest fixtures for setup, teardown, and environment initialization
├── logs/                    # Centralized log storage for all test runs
├── Pages/                   # Page Object Model (POM) classes for app screens
├── reports/                 # Test execution summary and exported reports
├── screenshots/             # Failure or validation screenshots captured during tests
├── Tests/                   # Test cases organized by features or modules
├── Utils/                   # Custom utilities (driver factory, Appium helpers, etc.)
├── conftest.py              # Global fixtures and hooks for pytest
├── pyproject.toml           # Project dependencies and tool configurations
└── pytest.ini               # Pytest configuration (markers, test paths, options)
```

---

## ⚙️ Key Features

* ✅ **Appium-based Mobile Automation** using Python client
* 🧱 **Page Object Model (POM)** for maintainable and reusable test design
* 🧪 **Pytest** integration for test organization, parametrization, and fixtures
* 📊 **Allure Reporting** for detailed HTML reports with screenshots and logs
* 🪄 **Custom Utilities** under `Utils/` for driver setup, logging, gestures, and common functions
* 📸 **Screenshot on Failure** mechanism for better debugging
* 🧾 **Centralized Logs** for tracking execution flow
* 🚀 **Modular & Scalable** structure ready for CI/CD integration

---

## 🧰 Prerequisites

Make sure you have the following installed:

* Python 3.9+
* Appium Server (v2.x recommended)
* Node.js (for Appium dependencies)
* Android SDK + Emulator setup
* Allure command-line tool (for report generation)

---

## ▶️ How to Run Tests

1. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```
2. **Start Appium server:**

   ```bash
   appium
   ```
3. **Execute tests with pytest:**

   ```bash
   pytest -m sanity --alluredir=allure-report
   ```
4. **View Allure report:**

   ```bash
   allure serve allure-report
   ```

---

## 🧩 Example Command Usage

Run a specific test with logging:

```bash
pytest Tests/test_login.py -v --log-cli-level=INFO
```

Run a suite with a tag:

```bash
pytest -m regression
```

---

## 📦 Folder Purpose Summary

| Folder/File      | Description                                               |
| ---------------- | --------------------------------------------------------- |
| `fixtures/`      | Common pytest fixtures for app and driver setup           |
| `Pages/`         | Page Object Model classes (App screens & elements)        |
| `Tests/`         | Test cases referencing page objects                       |
| `Utils/`         | Helper utilities (driver, actions, waits, config readers) |
| `logs/`          | Centralized execution logs                                |
| `reports/`       | Generated test reports                                    |
| `screenshots/`   | Screenshots captured during test failures                 |
| `allure-report/` | Auto-generated Allure results                             |
| `conftest.py`    | Global pytest hooks, fixtures, and configuration          |
| `pytest.ini`     | Pytest settings and markers                               |
| `pyproject.toml` | Dependency and tool configuration                         |

---

## 🧠 Future Enhancements

* Integrate with CI/CD (Jenkins, GitHub Actions, or GitLab CI)
* Add support for parallel execution
* Include API test layer integration (optional)
* Add retry logic with decorators for flaky tests
* Implement dynamic environment selection (e.g., staging, production)
