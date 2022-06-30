title: Parse in Python
date: 2022-06-10
description: Pyparsing module for beginners
tag: python
project: Python course for beginners
platform: Python Practicum
link: http://example.com

Parsing (syntactic analysis) is the process of matching a sequence of words or symbols - the so-called formal grammar. For example, for a line of code:

	import matplotlib.pyplot as plt


the following grammar takes place: first comes the keyword import, then the name of the module or a chain of module names separated by a dot, then the keyword as, followed by our name for the imported module.

As a result of parsing, for example, it may be necessary to arrive at the following expression:

	{ 'import': [ 'matplotlib', 'pyplot' ], 'as': 'plt' }


This expression is a Python dictionary that has two keys: 'import' and 'as'. The value for the 'import' key is a list that lists, in order, the names of the modules to be imported.

For parsing, as a rule, regular expressions are used. There is a Python module for this called re (regular expression). If you have never worked with regular expressions, their appearance may scare you. For example, for the line of code 'import matplotlib.pyplot as plt' it would be:

	r'^[ \t]*import +\D+\.\D+ +as \D+'