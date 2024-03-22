# Ex02 Django ORM Web Application
## Date: 22.3.24

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).




## Entity Relationship Diagram


![WhatsApp Image 2024-03-22 at 15 52 55_66d38c1f](https://github.com/pavi365/ORM/assets/115135775/c84358c3-1a90-402d-adb8-b5bca8e14256)


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
## MODELS.PY
from django.db import models
from django.contrib import admin
class Employee (models.Model):
    eid=models.IntegerField(primary_key=True)
    name=models.CharField(max_length=100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()
 
class EmployeeAdmin(admin.ModelAdmin):
    list_display=('eid','name','salary','age','email')

## ADMIN.PY
from django.contrib import admin
from .models import Employee,EmployeeAdmin
admin.site.register(Employee,EmployeeAdmin)
```

## OUTPUT
<img width="960" alt="image" src="https://github.com/pavi365/ORM/assets/115135775/eb240e94-6688-4f46-abfc-53fa324d97b1">


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
