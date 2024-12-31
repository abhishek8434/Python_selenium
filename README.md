# CLYMB_AUTOMATION

## Overview
This project is a Selenium-based test automation framework written in Python. It uses pytest as the testing framework and is designed to test the functionality of the CLYMB application.

## Project Structure
The project is organized as follows:

```
CLYMB_AUTOMATION/
|-- pages/                   # Page Object Model files
|   |-- login.py             # Login page functionality
|   |-- logout.py            # Logout page functionality
|
|-- tests/                   # Test cases
|   |-- __init__.py          # Marks this directory as a package
|   |-- clymb.py             # Tests for CLYMB
|   |-- clymbappreciation.py # Tests for appreciation functionality
|   |-- clymbfornegative.py  # Tests for negative conditions
|   |-- clymbtest.py         # General tests for CLYMB
|   |-- negative_conditions.py # Tests for negative condition scenarios
|
|-- utils/                   # Utility functions and shared logic
|   |-- aftermood.py         # Handles 'after mood' functionality
|   |-- appreciation.py      # Handles appreciation logic
|   |-- audio.py             # Audio-related utilities
|   |-- conditionfornegative.py # Negative condition utilities
|   |-- emotions_function.py # Emotion-related utilities
|   |-- locators.py          # Locators for web elements
|   |-- responsible_decision_making.py # Decision-making utilities
|   |-- self_management.py   # Self-management utilities
|   |-- social_awareness.py  # Social awareness utilities
|
|-- .env                     # Environment variables
|-- .gitignore               # Git ignore file
|-- README.md                # Project documentation
```

## Prerequisites
- Python 3.8 or higher
- Google Chrome or another supported browser
- ChromeDriver or the appropriate WebDriver for your browser

## Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd CLYMB_AUTOMATION
   ```

2. Set up a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Add a `.env` file for environment variables (e.g., base URL, credentials).

## Running Tests

To execute all tests:
```bash
pytest
```

To execute a specific test file:
```bash
pytest tests/<test_file_name>.py
```

To generate a detailed report:
```bash
pytest --html=report.html --self-contained-html
```
To generate a customized detailed report:
```bash
pytest --html=report.html --self-contained-html --metadata "Environment" "Production" --metadata "Tester" "Your Name"
```

## Key Features
- **Page Object Model (POM):** All web page interactions are encapsulated in the `pages` directory.
- **Reusable Utilities:** Commonly used functions and locators are located in the `utils` directory.
- **Environment Management:** Supports `.env` file for configurable variables.
- **Scalable Test Cases:** Organized in the `tests` directory, with dedicated files for specific features and scenarios.

## Contribution
1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your message here"
   ```
4. Push to your branch:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Open a pull request.

---

Happy Testing!
