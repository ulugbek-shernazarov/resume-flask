title: Flask from scratch
date: 2022-06-14
description: View functions and routes
tag: flash
project: Flask course for beginners
platform: Flask Workshop
link: http://example.com

You can get started with Flask by creating a simple application that prints "Hello World". Create a new main.py file and enter the following code.

	from flask import Flask

	app = Flask(__name__)

	@app.route('/')
	def index():
	return 'Hello World'

	if __name__ == "__main__":
	app.run()

This is a "Hello World" application built with the Flask framework. To run main.py, you need to run the following command:

	(env) python main.py
	Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)