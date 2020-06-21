### Starting a Django Project

```sh
$ mkdir source
$ cd source

$ python3 -m venv my_env
$ source my_env/bin/activate

$ pip3 install django
$ django-admin --version

$ django-admin startproject my_project .
$ cd my_project
$ python manage.py startapp blog
$ python manage.py runserver 0.0.0.0:8080

$ python manage.py makemigrations blog
$ python manage.py migrate blog


http://127.0.0.1:8000/
```

blog/models.py

```py
from django.conf import settings
from django.db import models
from django.utils import timezone


class Post(models.Model):
    author = models.ForeignKey(settings.AUTH_USER_MODEL, on_delete=models.CASCADE)
    title = models.CharField(max_length=200)
    text = models.TextField()
    created_date = models.DateTimeField(default=timezone.now)
    published_date = models.DateTimeField(blank=True, null=True)

    def publish(self):
        self.published_date = timezone.now()
        self.save()

    def __str__(self):
        return self.title
```

blog/admin.py

```py
from django.contrib import admin
from .models import Post

admin.site.register(Post)

# http://127.0.0.1:8000/admin/
```
### Create user

```py
$ python manage.py createsuperuser
```


