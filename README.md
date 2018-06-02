# hello_world_flask2.io
hello world in flask

#Getting started with flask
https://scotch.io/tutorials/getting-started-with-flask-a-python-microframework

#Installation
1.python
2.virtual env and virtualenvwrapper
3.Flask

We'll start by installing virtualenv, a tool to create isolated Python environments. We need to use virtual environments to keep the dependencies used by different Python projects separate, and to keep our global site-packages directory clean. We'll go one step further and install virtualenvwrapper, a set of extensions that make using virtualenv a whole lot easier by providing simpler commands.

$pip install virtualenv
$pip install virtualwrapper
$export WORKON_HOME=~/Envs
$ source /usr/local/bin/virtualenvwrapper.sh

To create and activate a virtualenv, run the following commands:
$ mkvirtualenv my-venv
$ workon my-venv

the other way to activate your virtual environment

Activate the virtual environment
You can activate the python environment by running the following command:

Mac OS / Linux
source my-venv/bin/activate

Windows
my-venv\Scripts\activate
You should see the name of your virtual environment in brackets on your terminal line e.g. (my-venv).

Any python commands you use will now work with your virtual environment

https://uoa-eresearch.github.io/eresearch-cookbook/recipe/2014/11/26/python-virtual-env/

Deactivate the virtual environment
To decativate the virtual environment and use your original Python environment, simply type ‘deactivate’.

deactivate

Next, let's create a directory for our app. This is where all our files will go:

$ mkdir my-project
$ cd my-project
Finally, let's install Flask:
$ pip install Flask

Installing Flask also installs a few other dependencies, which you will see when you run the following command:
$ pip freeze
click==6.6
Flask==0.11.1
itsdangerous==0.24
Jinja2==2.8
MarkupSafe==0.23
Werkzeug==0.11.11

What do all these packages do? Flask uses Click (Command Line Interface Creation Kit) for its command-line interface, which allows you to add custom shell commands for your app. ItsDangerous provides security when sending data using cryptographical signing. Jinja2 is a powerful template engine for Python, while MarkupSafe is a HTML string handling library. Werkzeug is a utility library for WSGI, a protocol that ensures web apps and web servers can communicate effectively.

You can save the output above in a file. This is good practice because anyone who wants to work on or run your project will need to know the dependencies to install. The following command will save the dependencies in a requirements.txt file:

pip freeze > requirements.txt

