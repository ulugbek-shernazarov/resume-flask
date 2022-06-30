title: Advanced Django
date: 2022-06-16
description: Understanding ORM in Django and working with the database without SQL queries
tag: django
project: Django Course - Level 2
platform: Django Workshop
link: http://example.com

Django ORM (Object Relational Mapping) is one of the most powerful features of Django. This allows us to interact with the database using Python code rather than SQL.

To demonstrate, I will describe the following model:

	from django.db import models

	class Blog(models.Model):
	name = models.CharField(max_length=250)
	url = models.URLField()

	def __str__(self):
	return self.name

	classAuthor(models.Model):
	name = models.CharField(max_length=250)

	def __str__(self):
	return self.name

	class Post(models.Model):
	title = models.CharField(max_length=250)
	content = models.TextField()
	published = models.BooleanField(default=True)
	blog = models.ForeignKey(Blog, on_delete=models.CASCADE)
	authors = models.ManyToManyField(Author, related_name="posts")