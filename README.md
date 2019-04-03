# Django-to-do


This is a sample project that a novice django developer can use to get started.

## Working



## Features

- Dead simple
- Easily add, delete
- Simple UI
- Blazing fast

## Setup

- Download the files from this repo
- Change the directory to the folder where you downloaded files
- For installing required packages, execute the following command in terminal:

    ```bash
    $pip install -r requirements.txt
    ```



Create a Database and Database User
```$sudo su - postgres```



You should now be in a shell session for the postgres user. Log into a Postgres session by typing:
```psql```



First, we will create a database for our Django project. We will call our database myproject
```CREATE DATABASE myproject;```



Next, we will create a database user which we will use to connect to and interact with the database. Set the password to something strong and secure:
```CREATE USER myprojectuser WITH PASSWORD 'password';```




We are setting the default encoding to UTF-8, which Django expects. We are also setting the default transaction isolation scheme to "read committed", which blocks reads from uncommitted transactions. Lastly, we are setting the timezone. By default, our Django projects will be set to use UTC:

```ALTER ROLE myprojectuser SET client_encoding TO 'utf8';```
```ALTER ROLE myprojectuser SET default_transaction_isolation TO 'read committed';```
```ALTER ROLE myprojectuser SET timezone TO 'UTC';```




- After successful installation execute the following commands:

    ```bash
    $python3 manage.py makemigrations
    $python3 manage.py migrate
    $python3 manage.py runserver
    ```
    
After creating the database structure, we can create an administrative account by typing:

```python manage.py createsuperuser```

You will be asked to select a username, provide an email address, and choose and confirm a password for the account.

- Visit `127.0.0.1:8000` in your browser to enjoy the awesome app!


