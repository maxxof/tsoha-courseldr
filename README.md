Welcome to Courseldry

---

Courseldry is an app where university students can review courses they have completed/attended to.
For now functionality and styling of the application is a little vacant but here's
the functions you can do as of now:

- Make an account and login, and of course, logout
- Read all the reviews that are stored in database
- Post a review

It is early stage of the application so visual appearance of the application wasn't
priority and more functionalities, like engagement with posts and unique user profiles
are yet to come.

---

Here's instructions on how to start the applicaton on your machine:

Clone this repository to your computer and move to the root directory of the application.
Create an `.env` file and paste following code there (NB: For some reason default port 
and/or host doesn't work properly on my machine so to avoid any complications I recommend
using these settings)

```
DATABASE_URL=<your-local-url>
SECRET_KEY=<some-random-numbers>
FLASK_RUN_HOST=0.0.0.0
FLASK_RUN_PORT=8000
```
P.S Local url (postgre) is usually either `postgresql:///<database-name>` or `postgresql+psycopg2://`.

Then you create virtual environment and download app dependencies with commands

```
$ python3 -m venv venv
$ source venv/bin/activate
$ pip install -r ./requirements.txt
```

Then define schema of your database

```
$ psql < schema.sql
```

Now you are ready to run the app:

```
$ flask run
```

---

Courseldry, 2023
