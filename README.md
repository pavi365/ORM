# Ex02 Django ORM Web Application
## Date: 22.3.24

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).
## Entity Relationship Diagram

![image](https://github.com/pavi365/ORM/assets/115135775/1d285731-92af-4c66-8a89-041b15e00664)



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
```
Models.py
from django.db import models
from django.contrib import admin
# Create your models here.
class BOOk(models.Model):
    book_id=models.IntegerField(primary_key=True)
    book_name=models.CharField(max_length=50)
    publisher_name=models.CharField(max_length=50)
    author_name=models.CharField(max_length=50)
    publish_year=models.DateField()

class BookAdmin(admin.ModelAdmin):
    list_display=('book_id','book_name','publisher_name','author_name','publish_year')

Admin.py
from django.contrib import admin
from .models import BOOk,BookAdmin
# Register your models here.

admin.site.register(BOOk,BookAdmin)

```

## OUTPUT
<img width="958" alt="image" src="https://github.com/pavi365/ORM/assets/115135775/9dc23227-05fd-4b47-be03-4795043e9dd7">



## RESULT
Thus the program for creating a database using ORM hass been executed successfully
