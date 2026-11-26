# Ex01 Django ORM Web Application
## Date:

## AIM
To develop a Django application to store and retrieve data from a Car Inventory Database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM



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
admin.py

from django.contrib import admin
from .models import Car,CarAdmin

admin.site.register(Car, CarAdmin)

```

```
Models.py


from django.db import models
from django.contrib import admin


class Car(models.Model):

    car_id = models.CharField(
        max_length=20,
        primary_key=True,
        help_text="Car ID"
    )

    brand = models.CharField(max_length=100)

    model = models.CharField(max_length=100)

    year = models.IntegerField()

    price = models.IntegerField()

    fuel_type = models.CharField(max_length=50)

    quantity = models.IntegerField()

    color = models.CharField(max_length=50)

    def __str__(self):
        return self.brand + " " + self.model


class CarAdmin(admin.ModelAdmin):

    list_display = (
        'car_id',
        'brand',
        'model',
        'year',
        'price',
        'fuel_type',
        'quantity',
        'color'
    )

```




## OUTPUT

<img width="1908" height="911" alt="Screenshot 2026-11-25 123311" src="https://github.com/user-attachments/assets/b7cb75ce-886a-4290-8392-03c7b68091a5" />



## RESULT
Thus the program for creating car inventory database database using ORM hass been executed successfully
