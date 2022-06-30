title: Getting Started with Flask
date: 2022-06-12
description: Understanding the main concepts and features of the framework
tag: flash
project: Flask course for beginners
platform: Flask Workshop
link: http://example.com

##Creating a Flask Application

Every Flask application must have an instance of the class. An instance is a WSGI application (WSGI is a server-to-framework interface) that indicates that the server is passing all received requests to the instance for further processing. The Flask class object is created like this:

from flask import Flask

app = Flask(__name__)

The first line imports the Flask class from the flask package.

The second line creates a Flask object. To do this, the Flask constructor is assigned the __name__ argument. The Flask constructor must have one required argument. They are the name of the package. In most cases, the __name__ value is fine. The app's package name is used by the Flask framework to find static files, templates, etc.

##Create route (paths)

A route (or path) is used in the Flask framework to bind a URL to a view function. This function responds to a request. In Flask, the route decorator is used to bind a URL to a function. Here is how the route is created.

@app.route('/')
def index():
return 'Hello World'

This code assigns the index() function as the root URL handler in the application. In other words, every time the application receives a request where the path is /, the index() function is called, and the request ends there.