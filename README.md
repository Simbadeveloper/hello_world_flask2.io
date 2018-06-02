# hello_world_flask2.io
hello world in flask

# Getting started with flask
https://scotch.io/tutorials/getting-started-with-flask-a-python-microframework

# Installation
We'll need the following installed for this tutorial:\n
1.python.\n
2.virtual env and virtualenvwrapper\n
3.Flask\n

We'll start by installing virtualenv, a tool to create isolated Python environments. We need to use virtual environments to keep the dependencies used by different Python projects separate, and to keep our global site-packages directory clean. We'll go one step further and install virtualenvwrapper, a set of extensions that make using virtualenv a whole lot easier by providing simpler commands.

#

$pip install virtualenv\n
$pip install virtualwrapper\n
$export WORKON_HOME=~/Envs\n
$ source /usr/local/bin/virtualenvwrapper.sh\n

To create and activate a virtualenv, run the following commands:
#

$ mkvirtualenv my-venv\n
$ workon my-venv\n

the other way to activate your virtual environment

Activate the virtual environment
You can activate the python environment by running the following command:
#

Mac OS / Linux\n
source my-venv/bin/activate\n

Windows
my-venv\Scripts\activate\n
You should see the name of your virtual environment in brackets on your terminal line e.g. (my-venv).\n

Any python commands you use will now work with your virtual environment

https://uoa-eresearch.github.io/eresearch-cookbook/recipe/2014/11/26/python-virtual-env/

Deactivate the virtual environment
To decativate the virtual environment and use your original Python environment, simply type ‘deactivate’.

deactivate

# Create a directory for your app
Next, let's create a directory for our app. This is where all our files will go:

$ mkdir my-project\n
$ cd my-project\n
Finally, let's install Flask:\n
$ pip install Flask\n

Installing Flask also installs a few other dependencies, which you will see when you run the following command:
#
$ pip freeze.\n
click==6.6.\n
Flask==0.11.1.\n
itsdangerous==0.24.\n
Jinja2==2.8.\n
MarkupSafe==0.23.\n
Werkzeug==0.11.11.\n

What do all these packages do? Flask uses Click (Command Line Interface Creation Kit) for its command-line interface, which allows you to add custom shell commands for your app. ItsDangerous provides security when sending data using cryptographical signing. Jinja2 is a powerful template engine for Python, while MarkupSafe is a HTML string handling library. Werkzeug is a utility library for WSGI, a protocol that ensures web apps and web servers can communicate effectively.

You can save the output above in a file. This is good practice because anyone who wants to work on or run your project will need to know the dependencies to install. The following command will save the dependencies in a requirements.txt file:
#
pip freeze > requirements.txt

