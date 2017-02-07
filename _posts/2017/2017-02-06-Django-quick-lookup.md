---
layout: post
title: Django Quick Lookup
date: 2017-02-06
tags: Django
category: [Tech]
comments: true

---

Django's documentation is large and here are the ones that might be frequently used by a Django beginner:

* [QuerySet API reference](https://docs.djangoproject.com/en/1.10/ref/models/querysets/)
  * Methods such as ```filter()```, ```exclude()```, ```order_by()``` that return a new QuerySet.
  * Methods such as ```get()```, ```create()```, ```count()``` that don't return a QuerySet.
  * Field lookups.

* [Request and response objects](https://docs.djangoproject.com/en/1.10/ref/request-response/)
  * The QueryDict objects(GET and POST in HttpRequest)

* [Managing static files (e.g. images, JavaScript, CSS)](https://docs.djangoproject.com/en/1.10/howto/static-files/)
  * [STATICFILES_FINDERS](https://docs.djangoproject.com/en/1.10/ref/settings/#std:setting-STATICFILES_FINDERS)

* [The Django template language](https://docs.djangoproject.com/en/1.10/ref/templates/language/)
  * [Built-in template tags and filters](https://docs.djangoproject.com/en/1.10/ref/templates/builtins/)
