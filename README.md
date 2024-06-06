# IMDBrainrot

This project is a moviedatabase with movies that does not make any sense. You can create a user with a login, and you can search up movies from our database consisting of 10000 movies!! Each movie has several attributes which describes them, and you can search these movies up.

For this project we have used the skeleton of the provided Green Groceries example, and we have modified it such that it fit the requirments of our own project.

## Initialization 

Clone / download repository files and navigate into the 'IMDBrainrot' folder and run the following to install the required packages:

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