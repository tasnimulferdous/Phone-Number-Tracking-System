# Phone Number Tracking System

## Project Overview
This project is a lightweight Python-based **Phone Number Tracking System** that extracts and displays key details about a phone number, including its time zone, carrier, and region of registration. Utilizing the `phonenumbers` library, the system provides a simple and efficient way to analyze phone numbers with minimal user input.

## Features
- **Time Zone Detection**: Identifies the time zone(s) associated with the phone number.
- **Carrier Identification**: Retrieves the name of the carrier providing service for the phone number.
- **Region Information**: Determines the geographical region where the phone number is registered.

## Requirements
- Python 3.x
- `phonenumbers` library (`pip install phonenumbers`)

## Installation
1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   ```
2. **Install Dependencies**:
   ```bash
   pip install phonenumbers
   ```
3. **Run the Script**:
   - Execute the main Python script (`phone_tracker.py`) and enter a phone number with its country code (e.g., +12025550123) when prompted.

## Usage
Run the script and input a phone number with the country code:
```bash
python phone_tracker.py
```
The system will output:
- The time zone(s) associated with the number.
- The carrier name (in English).
- The region where the number is registered.

## Example
```bash
Enter your NO. with country code: +12025550123
('America/New_York',)
Verizon
United States
```

## Code
The core script (`phone_tracker.py`) uses the `phonenumbers` library to parse and extract phone number details:
- Parses the input number using `phonenumbers.parse()`.
- Retrieves time zones with `timezone.time_zones_for_number()`.
- Identifies the carrier using `carrier.name_for_number()`.
- Determines the registration region with `geocoder.description_for_number()`.

## Limitations
- Requires a valid phone number with a country code.
- Accuracy depends on the `phonenumbers` library's database.
- No local file I/O or network calls are supported in this version to ensure compatibility with browser-based environments like Pyodide.

## Authors
Developed by Tasnimul Ferdous Tamim.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgments
Special thanks to the `phonenumbers` library maintainers for providing a robust tool for phone number analysis.
