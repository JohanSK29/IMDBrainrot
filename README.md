# IMDBrainrot

This project is a moviedatabase with movies that does not make any sense. You can create a user with a login, and you can search up movies from our database consisting of 10000 movies!! Each movie has several attributes which describes them, and you can search these movies up.

For this project we have used the skeleton of the provided Green Groceries example, and we have modified it such that it fit the requirments of our own project.

## Initialization 

Clone / download repository files and run the following to install the required packages:

    pip install -r requirements.txt

Create a new database in pgAdmin (preferably named IMDBrainrot) and add the following to your .env file:

    SECRET_KEY=<secret_key>
    DB_USERNAME=postgres || <postgres_user_name>
    DB_PASSWORD=<postgres_user_password>
    DB_NAME=IMDBrainrot || <postgres_db_name>

When all this information is present (and correct) the server can be started with:

    flask run


## Regular expression

The regular expression that we have is one on the login page. When you create a user, we have made a regular expression that matches the passwords. Your password HAS to have at least one capital letter and at least one number in it. Furthermore the password can be a maximum of 15 characters long.


## E/R diagram

Our E/R diagram is provided as a picture here in the Github.

## Folder setup 📁

The app is divided into multiple folders similar to the structure of the example project, with a few tweaks:

- __blueprints__: Contains all the separate blueprints of the app (submodules of the app the store different parts of
  the functionality)
- __dataset__: Contains the csv file used to import the produce data
- __static__: Contains static files like images, css and js files (in this case javascript was not needed in the
  frontend)
- __templates__: This is the template folder of the app that stores all html files that are displayed in the user
  browser
- __utils__: Contains the sql files and script that generate the postgresql database. Also contains a script that
  generates custom choices objects for flask forms used in SelectFields taken from the dataset.

At the root folder of the app (./IMDBrainrot) six more scripts are present with the following roles:

- __\_\_init\_\_.py__: Initializes the flask app and creates a connection to the database (and a cursor object for
  future queries)
- __app.py__: Runs the app created by \_\_init__.py
- __filters.py__: Implements custom template filters for nicer formatting of data in the frontend
- __forms.py__: Implements forms used to save data from users (similar to the example project)
- __models.py__: Implements custom classes for each of the database tables to store data in a clean OOP manner (again,
  similar to the example project, but our models inherit the dict class for faster and more readable lookups)
- __queries.py__: Implements functions for each needed query to the database used inside the app (similar to the
  functional part of the models.py file within the example project)

## Routes

Both implemented blueprints come with a __routes.py__ file that initialize a __Blueprint__ object and define _routes_
for the app.

- __Login__:
    - __/home__: Home page
    - __/about__: About page
    - __/style-guide__: Style guide (displays all html elements used, just for fun and css debugging)
    - __/login__: User login page (for simplicity in debugging, password hashing was omitted even though the example
      project made it pretty clear and easy to implement with bcrypt)
    - __/signup__: User signup (creation) page
    - __/logout__: Logs user out and sends back to login page


