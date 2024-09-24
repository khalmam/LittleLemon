# LittleLemon Backend Application

This project **LittleLemon** is part of the Backend Developer Capstone Project by Meta. It is a backend application designed with Django, Django REST Framework, Djoser for authentication, and MySQL as the main database. The goal of this project is to build a fully functional backend site with RESTful APIs.

## Table of Contents
- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)

## Project Overview
LittleLemon is a backend application that provides APIs for handling various site functionalities. The project is built as part of the **Meta Backend Developer Capstone Project**, which involves the development of a robust backend site using Django and related technologies. The main features include:
- Authentication with **Djoser**.
- RESTful APIs powered by **Django REST Framework**.
- Database management using **MySQL**.

## Technologies Used
- **Django**: A high-level Python web framework.
- **Django REST Framework (DRF)**: A powerful toolkit for building Web APIs.
- **Djoser**: A RESTful authentication library for Django projects.
- **MySQL**: The primary database used to store and manage application data.

## Installation

### Prerequisites
Ensure you have the following installed on your system:
- Python 3.x
- MySQL
- Pip (Python package installer)

### Steps
1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/Littlelemon.git
   cd littlelemon-backend

2. **Set up a virtual environment**:
```bash
python -m venv env
source env/bin/activate  # For Windows use `env\Scripts\activate`
```

3. **Install dependencies**:

```bash
pip install -r requirements.txt
```
4. **Configure the database**: Create a MySQL database and update the DATABASES settings in the settings.py file:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'your_db_name',
        'USER': 'your_db_user',
        'PASSWORD': 'your_db_password',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
```
5. **Run migrations**:

```bash
python manage.py makemigrations
python manage.py migrate
```
6. **Create superuser**:

```bash
python manage.py createsuperuser
```

7. **Run the development server**:

```bash
python manage.py runserver
```

## API Endpoints
Here are some of the key endpoints available in the LittleLemon API:

- **Authentication**:
  - `POST /auth/users/` – Register a new user.
  - `POST /api-token-auth/` – Get an authentication token.
  - `POST /auth/token/login/` – Log in a user using the Djoser endpoint.

- **Menu Items**:
  - `GET /restaurant/menu/` – Retrieve a list of menu items.
  - `GET /restaurant/menu/{menuItemId}` – Retrieve a specific menu item by ID.

- **Table Booking**:
  - `GET /restaurant/booking/tables/` – View all available table bookings.
  - `GET /restaurant/booking/tables/{bookingId}` – View a specific table booking by ID.

## Guiding Principles
The development of LittleLemon follows several guiding principles, including:
1. **Modularity**: Keep the application modular and maintainable, following Django’s best practices.
2. **RESTful API Design**: The API follows REST conventions, ensuring clean and intuitive endpoints.
3. **Security**: Use Djoser for secure authentication, ensuring the security of user data and API access.
4. **Scalability**: Ensure the application can scale and integrate with other services if necessary.
5. **Performance**: Optimize queries and API responses for better performance.

## Contributors
This project was built by Ibrahim Imam as part of Meta's Backend Developer Capstone Project.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

