Waist Measurement App
# Table of Contents
Features
Installation
Usage
Code Structure
Contributing
License
# Features
## User Authentication
Secure sign-up and login functionality.
Passwords are hashed using werkzeug.security for enhanced security.
## Patient Management
Add new patient records with details such as:
- Patient ID
- Name
- Blood pressure
- Heart rate
- Height (cm)
- Weight (kg)
- Waist measurement (cm)
- Smoking, drinking, and exercise habits
- Free-text notes
View and search through existing patient records.
Delete patient records securely.
## Waist Measurement Calculator
Estimate waist measurements based on:
- Age (18–70 years)
- Gender (Male/Female)
- Height (cm)
- Weight (kg)
- Body type (Slim, Normal, Mild Obesity, Obese)
Provides cardiovascular risk warnings if the calculated waist measurement exceeds thresholds:
- Male: ≥ 102 cm
- Female: ≥ 88 cm
## Multilingual Support
Switch seamlessly between English and Turkish.
# Installation
## Prerequisites
- Python 3.x
- Pip (Python package manager)
## Steps
Clone the repository:
```bash
git clone https://github.com/your-username/waist-measurement-app.git
cd waist-measurement-app
```
Install the required dependencies:
```bash
pip install -r requirements.txt
```
Run the application:
```bash
python app.py
```
Access the app in your browser at http://localhost:8080.
# Usage
## Sign-Up/Login
- Create an account or log in using your credentials.
## Dashboard
- Add new patient records.
- Use the waist measurement calculator.
- View, search, and delete patient records.
## Language Switching
- Toggle between English and Turkish using the language flags.
## Waist Calculator
- Input details such as age, gender, height, weight, and body type to calculate waist measurements and view cardiovascular risk warnings.
# Code Structure
The project is organized into the following components:
## Models
- **User**: Stores user authentication details (username, email, password).
- **Patient**: Stores patient records (ID, name, blood pressure, heart rate, height, weight, etc.).
## Routes
- `/signup`: Handles user registration.
- `/login`: Handles user login.
- `/dashboard`: Displays the main dashboard with patient management and waist calculator.
- `/delete_patient/<patient_id>`: Deletes a specific patient record.
## Templates
HTML templates (HTML_HOME, HTML_SIGNUP, HTML_LOGIN, HTML_DASHBOARD) are rendered dynamically using Flask's `render_template_string`.
## Translations
Multilingual support is implemented using Flask-Babel with translations stored in `.po` files.
# Contributing
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m 'Add feature/fix'
   ```
4. Push to your branch:
   ```bash
   git push origin feature-name
   ```
5. Open a pull request.
# License
This project is licensed under the MIT License. See the LICENSE file for more details.
# Acknowledgments
Developed by Dr. Phyo Paing Aye.
Built using Flask, Flask-SQLAlchemy, Flask-Babel, and other open-source libraries.
