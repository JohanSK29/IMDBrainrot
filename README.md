# IMDBrainrot

This project is a moviedatabase with movies that does not make any sense. You can create a user with a login, and you can search up movies from our database consisting of 10000 movies!! Each movie has several attributes which describes them, and you can then filter movies and find the movies which you want to see.

For this project we have used the skeleton of the provided Green Groceries example, and we have modified it such that it fit the requirments of our own project.

## Initialization 

Clone / download repository files and navigate into the 'IMDBrainrot' folder and run the following to install the required packages:

    pip install -r requirements.txt

Navigate into the utils folder, and run init_db.py to initialize the project.

    python init_db.py

Navigate back into the IMDBrainrot folder and run the application using:

    flask run

Ignore the folder which is called env, and navigate only into the IMDBrainrot folder

## Regular expression

The regular expression that we have is one on the login page. When you create a user, we have made a regular expression that matches the passwords. Your password HAS to have at least one capital letter and at least one number in it. Furthermore the password can be a maximum of 15 characters long.


## E/R diagram

Our E/R diagram is provided as a picture here in the Github.
