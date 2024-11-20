# mobile-automation-framework

## Overview
This framework is designed for mobile application automation using Appium. It follows the Page Object Model (POM) design pattern, ensuring modularity and maintainability. The framework is built with Python and integrates Pytest for test execution.

---

## Features
- **Page Object Model (POM):** Ensures reusable and maintainable code.
- **Configurable:** Easy-to-modify capabilities via JSON and YAML.
- **Cross-platform Support:** Works with Android and iOS.
- **Logging Utility:** Provides detailed logs for debugging.
- **Reports:** Supports HTML test reports.

---

## Prerequisites

1. **Install Python:**
   Ensure Python 3.7 or later is installed on your system.
   ```bash
   python --version
Install Node.js: Appium requires Node.js. Install it if it's not already available.

bash
Copy code
node --version
Install Appium: Install Appium globally using npm.

bash
Copy code
npm install -g appium
Install Device/Platform SDKs:

For Android: Ensure the Android SDK is installed and configured.
For iOS: Ensure Xcode is installed and configured.
Install Python Dependencies: Install the required Python packages listed in requirements.txt.

bash
Copy code
pip install -r requirements.txt
Start Appium Server: Ensure the Appium server is running before executing the tests.

bash
Copy code
appium
Configuration
Edit capabilities.json: Update the file with your device and app details.

json
Copy code
{
  "platformName": "Android",
  "platformVersion": "11.0",
  "deviceName": "emulator-5554",
  "app": "/path/to/your/app.apk",
  "automationName": "UiAutomator2"
}
Edit config.yaml: Update the Appium server URL and other configurations if necessary.

yaml
Copy code
app_url: "http://localhost:4723/wd/hub"
timeout: 30
Framework Structure
bash
Copy code
MobileAutomationFramework/
├── config/
│   ├── capabilities.json   # Appium capabilities configuration
│   ├── config.yaml         # Framework configuration
├── drivers/
│   ├── driver_factory.py   # Handles driver setup and teardown
├── pages/
│   ├── base_page.py        # Base Page Object class
│   ├── login_page.py       # Login Page Object
├── tests/
│   ├── test_login.py       # Sample test for login
├── utils/
│   ├── logger.py           # Logging utility
├── requirements.txt        # Python dependencies
├── README.md               # Documentation
Running Tests
Run All Tests: Execute all tests in the tests/ folder.

bash

pytest tests/
Run a Specific Test: Execute a specific test file.

bash

pytest tests/test_login.py
Generate HTML Report: Generate a test execution report.

bash

pytest --html=reports/report.html
Debugging
Appium Logs: Check the Appium server logs for detailed execution information.
Framework Logs: Logs are available in the console during test execution.
Contribution
Feel free to fork this repository, add features, fix bugs, or suggest improvements. Contributions are welcome!



