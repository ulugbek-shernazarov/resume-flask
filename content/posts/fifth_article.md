title: How Flask Handles Requests
date: 2022-06-17
description: Flask routing and the route decorator
tag: flash
project: Flask course for beginners
platform: Flask Workshop
link: http://example.com

How does Flask know which function to output when it receives a request from a client?

Flask maps the URL and render functions to be rendered. The mapping definition (routing) is created using the route decorator or the add_url_rule() method on a Flask instance. These mappings can be accessed using the url_map attribute on the Flask instance.

	>>>
	>>> from main2 import app
	>>> app.url_map
	Map([<Rule '/' (OPTIONS, GET, HEAD) -> index>,
	<Rule '/static/<filename>' (OPTIONS, GET, HEAD) -> static>,
	<Rule '/books/<genre>' (OPTIONS, GET, HEAD) -> books>,
	<Rule '/user/<user_id>' (OPTIONS, GET, HEAD) -> user_profile>])
	>>>

As you can see, there are 4 rules. Flask defines URL matches in the following format:

	url pattern, (comma separated list of HTTP methods handled by the route) -> view function to execute

The path /static/<filename> is automatically added for static files by Flask. Working with static files will be discussed in a separate lesson "Serving static files in Flask".