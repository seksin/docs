title: Flask Dashboard Now UI

# [Flask Dashboard](http://appseed.us/admin-dashboards/flask) - [Now UI](https://appseed.us/admin-dashboards/flask-dashboard-nowui-design)

**Open-Source Admin Dashboard** coded in **[Flask Framework](https://palletsprojects.com/p/flask/)** on top of **NowUI Dashboard** design (free version) - Provided by **AppSeed** [Web App Generator](https://appseed.us/app-generator).

## Dashboard Features
---

- UI-Ready, SQLite database
- SQLAlchemy ORM
- Session-Based authentication flow (login, register)
- Forms validation
- UI Kit: **[NowUI Dashboard](https://flask-now-ui-dashboard.appseed.us/login.html)** (Free version) provided by **Creative-Tim**
- **MIT License**
- Support: Free support via **Github** and (Paid) **24/7 LIVE Support** via [Discord](https://discord.gg/fZC6hup)

<br />

## Dashboard Links
---

- [Flask Dashboard Now UI](https://appseed.us/admin-dashboards/flask-dashboard-nowui-design) - Product page
- [Flask Dashboard Now UI](https://github.com/app-generator/flask-now-ui-dashboard/) - Source Code
- [Flask Dashboard Now UI](https://flask-now-ui-dashboard.appseed.us/login.html) - LIVE Demo

<br />

![Flask Dashboard Now UI - Open-Source Admin Panel](https://raw.githubusercontent.com/app-generator/static/master/products/flask-dashboard-nowui-design-screen.png)

<br />

## Prepare your environment
---

The product is built on top of [Flask](https://palletsprojects.com/p/flask/), a popular Python Web Framework. To build the app, Python3 should be installed properly in the workstation. If you are not sure if Python is properly installed, please open a terminal and type `python --version`. The full-list with dependencies and tools required to build the app:

- [Python3](https://www.python.org/) - the programming language used to code the app
- [Git](https://git-scm.com/) - used to clone the source code from the Github repository
- A [Github](https://github.com/) account - the invitation to the source code, will be sent on your account.
- Basic development tools (g++ compiler, python development libraries ..etc) used by Python to compile the app dependencies in your environment.

<br />

> Check Python (using the terminal)

```bash
$ # Check Python version
$ python --version
Python 3.7.2 # <--- All good
```

<br />

> Check GIT command tool (using the terminal)

```bash
$ # Check git
$ git --version
$ git version 2.10.1.windows.1 # <--- All good
```

<br />

For more information on how to set up your environment please access the resources listed below. In case we've missed something, contact us on Discord.

- [How to set up Python](/how-to/install-python)
- [Setup CentOS for development](/how-to/setup-centos-for-development/)
- [Setup Ubuntu for development](/how-to/setup-ubuntu-for-development/)
- [Setup Windows for development](/how-to/setup-windows-for-development/)

<br />

## Project Structure
---

The boilerplate code is built with a modular structure that follows the recommended pattern used by many open-source projects. The most important files and  directories are shown below:

<br />

```bash
< PROJECT ROOT >                          # application root folder
    |
    |--- app/__init__.py                  # application constructor  
    |--- app//assets                      # Img, CSS, Javascript files
    |--- app/templates                    # Jinja2 files
    |            |---<includes>           # Page chunks, components
    |            |---<layouts>            # Layouts
    |            |---<pages>              # Pages
    |                |---- index.html     # Main dashboard page
    |                |---- login.html     # Login page
    |                |---- register.html  # Registration Page
    |                |---- tables.html    # UI Tables
    |                |---- charts.html    # Charts
    |
    |--- requirements.txt                 # Modules and dependencies
    |
    |--- run.py                           # bootstrap the app
    |
    |-----------------------------
```

<br />

## Build from sources
---

```bash
$ # Clone the sources
$ git clone https://github.com/app-generator/flask-now-ui-dashboard.git
$ cd flask-now-ui-dashboard
$
$ # Virtualenv modules installation (Unix based systems)
$ virtualenv --no-site-packages env
$ source env/bin/activate
$
$ # Virtualenv modules installation (Windows based systems)
$ # virtualenv --no-site-packages env
$ # .\env\Scripts\activate
$ 
$ # Install requirements
$ pip3 install -r requirements.txt
$
$ # Set the FLASK_APP environment variable
$ (Unix/Mac) export FLASK_APP=run.py
$ (Windows) set FLASK_APP=run.py
$ (Powershell) $env:FLASK_APP = ".\run.py"
$
$ # Set up the DEBUG environment
$ # (Unix/Mac) export FLASK_ENV=development
$ # (Windows) set FLASK_ENV=development
$ # (Powershell) $env:FLASK_ENV = "development"
$
$ # Run the application
$ # --host=0.0.0.0 - expose the app on all network interfaces (default 127.0.0.1)
$ # --port=5000    - specify the app port (default 5000)  
$ flask run --host=0.0.0.0 --port=5000
$
$ # Access the app in browser: http://127.0.0.1:5000/
```

<br />

## Deployment
---

The app is provided with a basic configuration to be executed in [Docker](https://www.docker.com/), [Gunicorn](https://gunicorn.org/), and [Waitress](https://docs.pylonsproject.org/projects/waitress/en/stable/).

<br />

### [Docker](https://www.docker.com/) execution
---

The application can be easily executed in a docker container. The steps:

> Get the code

```bash
$ git clone https://github.com/app-generator/flask-dashboard-adminator.git
$ cd flask-dashboard-adminator
```

> Start the app in Docker

```bash
$ sudo docker-compose pull && sudo docker-compose build && sudo docker-compose up -d
```

Visit `http://localhost:5005` in your browser. The app should be up & running.

<br />

### [Gunicorn](https://gunicorn.org/)
---

Gunicorn 'Green Unicorn' is a Python WSGI HTTP Server for UNIX.

> Install using pip

```bash
$ pip install gunicorn
```
> Start the app using gunicorn binary

```bash
$ gunicorn --bind 0.0.0.0:8001 run:app
Serving on http://localhost:8001
```

Visit `http://localhost:8001` in your browser. The app should be up & running.


<br />

### [Waitress](https://docs.pylonsproject.org/projects/waitress/en/stable/)
---

Waitress (Gunicorn equivalent for Windows) is meant to be a production-quality pure-Python WSGI server with very acceptable performance. It has no dependencies except ones that live in the Python standard library.

> Install using pip

```bash
$ pip install waitress
```
> Start the app using [waitress-serve](https://docs.pylonsproject.org/projects/waitress/en/stable/runner.html)

```bash
$ waitress-serve --port=8001 run:app
Serving on http://localhost:8001
```

Visit `http://localhost:8001` in your browser. The app should be up & running.

<br />

## Flask Dashboard NowUI - App screens
---

<br />

![Flask Dashboard Adminator - User Profile Page.](https://raw.githubusercontent.com/app-generator/static/master/products/flask-dashboard-nowui-design-screen-1.png)

<br />

![Flask Dashboard Adminator - UI Notifications Page.](https://raw.githubusercontent.com/app-generator/static/master/products/flask-dashboard-nowui-design-screen-2.png)

<br />

![Flask Dashboard Adminator - Nucleo Icons Page.](https://raw.githubusercontent.com/app-generator/static/master/products/flask-dashboard-nowui-design-screen-3.png)

<br />

## Credits & Links
---

<br />

### [Flask Framework](https://www.palletsprojects.com/p/flask/)

[Flask](/what-is/flask) is a micro web framework written in Python. It is classified as a microframework because it does not require particular tools or libraries. It has no database abstraction layer, form validation, or any other components where pre-existing third-party libraries provide common functions.

<br />

## [What is dashboard](https://en.wikipedia.org/wiki/Dashboard_(business))

In information technology, a **[dashboard](https://en.wikipedia.org/wiki/Dashboard_(business))** is a user interface that, somewhat resembling an automobile's dashboard, organizes and presents information in a way that is easy to read. However, a computer dashboard is more likely to be interactive than an automobile dashboard (unless it is also computer-based). To some extent, most graphical user interfaces (GUIs) resemble a dashboard - by [Techtarget](https://searchcio.techtarget.com/definition/dashboard)

<br />

### [Now UI Dashboard](https://www.creative-tim.com/product/now-ui-dashboard)

Now UI Dashboard is a responsive Bootstrap 4 kit provided for free by Invision and Creative Tim. It combines colors that are easy on the eye, spacious cards, beautiful typography, and graphics. Now UI Dashboard comes packed with all plugins that you might need inside a project and documentation on how to get started - provided by **Creative-Tim**.

<br />

---
[Flask Dashboard Now UI](https://appseed.us/admin-dashboards/flask-dashboard-nowui-design) - Provided by AppSeed [Web App Generator](https://appseed.us/app-generator).
