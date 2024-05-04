# MailerHive
MailerHive is a robust Django-based API designed for efficient email management and distribution. It facilitates sending emails to both single and multiple recipients seamlessly. With features for SMTP configuration and error handling, MailerHive streamlines email communication and management tasks with ease and reliability.

## Features

- &#10003; **SMTP Configuration Management :** Configure SMTP settings via API endpoints.
- &#10003; **Email Composition :** Compose and send emails with single or multiple recipients.
- &#10003; **Error Handling :** Robust error handling for various email-related scenarios.


## Getting Started
Follow these instructions to set up and use MailerHive.

## Prerequisites

Before you begin, ensure you have the following installed:

- &#10003; Python (3.x recommended)
- &#10003; Django
- &#10003; Django Rest Framework

## Installation

1. **Clone the repository :**

   ```bash
   git clone https://github.com/Shashi2632/MailerHive.git
2. **Navigate to the project directory :**

   ```bash
   cd mailerhive
3. **Install dependencies :**  

   ```bash
   pip install -r requirements.txt

## Configuration

1. **Set up your database in Django ( `settings.py` ):**

   Ensure your database settings are configured correctly in the `settings.py` file of your Django project.

2. **Run migrations:**

   ```bash
   python manage.py migrate

## Usage

1. **Configure SMTP Settings:**
  Use the `/api/smtp/settings` endpoint to configure SMTP settings.

2. **Compose and Send Emails:**
  Use the `/api/send-mail` endpoint to compose and send emails.

  - **Parameters:**
    - `subject`: Subject of the email.
    - `message`: Body/content of the email.
    - `recipientType`: Type of recipient ( `single` or `multiple` ).
    - `recipient`: Email address ( `for single recipient` ).
    - `recipientFile`: Uploaded file containing multiple recipients ( `for multiple recipients` ).

## Endpoints

- **GET /api/smtp/settings :** Retrieve SMTP settings.

- **POST /api/smtp/settings :** Set/update SMTP settings.

- **POST /api/send-mail :** Compose and send emails.

## Error Handling

- **Invalid Email Addresses :**
  Ensure that valid email addresses are provided.

- **Missing SMTP Configuration :**
  Set up SMTP settings before sending emails.

## Contributing

Contributions are welcome! Feel free to open issues or pull requests for feature requests, bug fixes, or improvements.

## License

This project is licensed under the <a href="https://opensource.org/licenses/MIT" style="color: blue; text-decoration: none;">MIT License</a>.
