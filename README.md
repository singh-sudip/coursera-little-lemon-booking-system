# Full Stack Little Lemon Restaurant Booking System

This is a full-stack restaurant booking system, which is developed using Django framework, JavaScript, HTML, CSS, and MySQL database as part of a Meta Back-End Developer Developer Professional Certificate course to acquire the necessary skills for becoming a full-stack developer. The project utilizes Django Rest Framework, also known as DRF, for building API(s).

## Installation and Setup

### Pre-requisites

- Install Python - [https://www.python.org/downloads/](https://www.python.org/downloads/)
- Install pipenv - `pip3 install pipenv` - allows you to create a virtual environment for the project in order to isolate the project specific dependencies from the global scope, or other Python projects.
- Install MySQL - [https://www.mysql.com/downloads/](https://www.mysql.com/downloads/). Or install MySQL using [Homebrew](https://brew.sh/)
- Start / Run the MySQL server
- Create a MySQL database named (for example, `little_lemon_db`) with the following command: `CREATE DATABASE little_lemon_db;`

## Running the app

To install the app, clone the repository, and run the following command in the root directory of the project:

1. Clone the repository

If using SSH authentication:

```shell
git clone git@github.com:singh-sudip/coursera-little-lemon-booking-system.git
```

or, if using HTTPS authentication:

```shell
git clone https://github.com/singh-sudip/coursera-little-lemon-booking-system.git
```

or, if using GitHub CLI:

```shell
gh repo clone singh-sudip/coursera-little-lemon-booking-system
```

2. cd into the project directory. For this project, it will be:

```shell
cd coursera-little-lemon-booking-system
```

3. Create a virtual environment for the project via the terminal

```shell
pipenv shell
```

4. Install the dependencies via the terminal

```shell
pipenv install
```

5. Configure the local MySQL database setting values in `littlelemon/settings.py` file. The default values are as follows:

```python
# settings.py

DATABASES = {
    "default": {
        "ENGINE": "django.db.backends.mysql",
        "NAME": "little_lemon_db_name", # name of MySQL database
        "HOST": "127.0.0.1", # MySQL server host, either localhost or 127.0.0.1 for local machine
        "PORT": "3306", # MySQL server port. default value is 3306.
        "USER": "little_lemon_db_user", # MySQL user which has access to the database for performing various operations
        "PASSWORD": "little_lemon_db_pwd", # MySQL user password to connect to the database
    }
}
```

**Note**: to create MySQL user and grant privileges, run the following SQL commands:

```sql
CREATE USER 'little_lemon_db_user'@'localhost' IDENTIFIED BY 'little_lemon_db_pwd';
GRANT ALL PRIVILEGES ON little_lemon_db_name.* TO 'little_lemon_db_user'@'localhost';
FLUSH PRIVILEGES;
```

6. Run the individual migration commands in your terminal to create the necessary database tables in the MySQL database (**_little_lemon_db_name_**):

```shell
python3 manage.py makemigrations
python3 manage.py migrate
```

7. Run the following command to start the Django development server:

```shell
python3 manage.py runserver
```

The default port is 8000. If you wish to run the Django app on a different port, 8080, use the following command:

```shell
python3 manage.py runserver 8080
```

## Technologies Used

- Python
- Django
- Django REST Framework (DRF)
- Djoser (for authentication)
- MySQL
- HTML
- CSS
- JavaScript
