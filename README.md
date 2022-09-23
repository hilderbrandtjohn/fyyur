## Fyyur
-----

## Introduction

Fyyur is a musical venue and artist booking site that facilitates the discovery and bookings of shows between local performing artists and venues. This site lets you list new artists and venues, discover them, and list shows with artists as a venue owner.

## Overview

This app is a fully functioning site that is at capable of doing the following, and more, using a PostgreSQL database:

* creating new venues, artists, and creating new shows.
* searching for venues and artists.
* learning more about a specific artist or venue.

## Tech Stack (Dependencies)

### 1. Backend Dependencies
The tech stack includes the following:
 * **virtualenv** as a tool to create isolated Python environments
 ```
 pip install virtualenv
 ```
 * **SQLAlchemy ORM** to be our ORM library of choice
 ```
 pip install SQLAlchemy
 ```
 * **PostgreSQL** as our database of choice
  ```
  pip install postgres
  ```
 * **Python3** and **Flask** as our server language and server framework
  ```
  pip install Flask
  ```
 * **Flask-Migrate** for creating and running schema migrations
  ```
  pip install Flask-Migrate
  ```
### 2. Frontend Dependencies
You must have the **HTML**, **CSS**, and **Javascript** with [Bootstrap 3](https://getbootstrap.com/docs/3.4/customize/) for the website's frontend. Bootstrap can only be installed by Node Package Manager (NPM). 
Download and install the [Node.js](https://nodejs.org/en/download/). Windows users must run the executable as an Administrator, and restart the computer after installation. 
After successfully installing the Node, verify the installation using:
```
node -v
npm -v
```
Install [Bootstrap 3](https://getbootstrap.com/docs/3.3/getting-started/) for the website's frontend:
```
npm init -y
npm install bootstrap@3
  ```
-----

## Application Setup
1. **Download the project code locally**
```
git clone https://github.com/hilderbrandtjohn/fyyur.git
```

2. **Initialize and activate a virtualenv using:**
```
python -m virtualenv env
source env/bin/activate
```
>**Note** - In Windows, the `env` does not have a `bin` directory. Therefore, you'd use the analogous command shown below:
```
source env/Scripts/activate
```

3. **Install the dependencies:**
```
pip install -r requirements.txt
```

4. **Run the development server:**
```
export FLASK_APP=myapp
export FLASK_ENV=development # enables debug mode
python3 app.py
```

5. **Verify on the Browser**<br>
Navigate to project homepage [http://127.0.0.1:5000/](http://127.0.0.1:5000/) or [http://localhost:5000](http://localhost:5000) 

----
Overall:
* Models are located in the `MODELS` section of `app.py`.
* Controllers are also located in `app.py`.
* The web frontend is located in `templates/`, which builds static assets deployed to the web server at `static/`.
* Web forms for creating data are located in `form.py`


Highlight folders:
* `templates/pages` -- Defines the pages that are rendered to the site. These templates render views based on data passed into the template’s view, in the controllers defined in `app.py`. These pages successfully represent the data to the user, and are already defined for you.
* `templates/layouts` -- Defines the layout that a page can be contained in to define footer and header code for a given page.
* `templates/forms` -- Defines the forms used to create new artists, shows, and venues.
* `app.py` -- Defines routes that match the user’s URL, and controllers which handle data and renders views to the user.
* Models in `app.py` --Defines the data models that set up the database tables.
* `config.py` -- Stores configuration variables and instructions, separate from the main application code. 



