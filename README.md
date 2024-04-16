# Ex02 Django ORM Web Application
## Date: 05-04-2024

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM

ADMIN.PY
```
from django.contrib import admin
from .models import BOOK,BOOKAdmin
admin.site.register(BOOK,BOOKAdmin)

```
MODELS.PY
```
from django.db import models
from django.contrib import admin
class BOOK(models.Model):
    BOOK_TITLE=models.CharField(max_length=50,primary_key=True);
    BOOK_PAGES=models.IntegerField();
    BOOK_AUTHOR=models.CharField(max_length=50);
    BOOK_PRICE=models.DecimalField(max_digits=10,decimal_places=True);
    BOOK_CHAPTER=models.CharField(max_length=50);
class BOOKAdmin(admin.ModelAdmin):
    list_display=("BOOK_TITLE","BOOK_PAGES","BOOK_AUTHOR","BOOK_PRICE","BOOK_CHAPTER");
```

## OUTPUT

![alt text](34c326fa-7936-4975-b600-83baa31d815b.jpg)

## RESULT
Thus the program for creating a database using ORM hass been executed successfully
