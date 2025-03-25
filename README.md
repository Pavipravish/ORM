# Ex02 Django ORM Web Application
# Date:25/03/2025
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# ENTITY RELATIONSHIP DIAGRAM
## DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py
from django.contrib import admin

from django.contrib import admin

# Register your models here.
from .models import Loan,LoanAdmin

admin.site.register(Loan,LoanAdmin)  
## STEP 4:
Execute Django admin and create details for 10 books

# PROGRAM
admins.py
    from django.contrib import admin
    
    from django.contrib import admin
    from .models import Loan,LoanAdmin
    
    admin.site.register(Loan,LoanAdmin)  

models.py
    from django.db import models
    from django.contrib import admin
    
    class Loan(models.Model):
        loan_id = models.AutoField(primary_key=True)
        customer_name = models.CharField(max_length=100)
        loan_amount = models.DecimalField(max_digits=10, decimal_places=2)
        interest_rate = models.DecimalField(max_digits=5, decimal_places=2)
        loan_term = models.IntegerField()
        disbursement_date = models.DateField()
    
    class LoanAdmin(admin.ModelAdmin):
        list_display=('loan_id','customer_name','loan_amount','interest_rate','loan_term','disbursement_date')

# ER DIAGRAM
![Screenshot 2024-12-06 105339](https://github.com/user-attachments/assets/f8331d4b-5a40-49fd-839c-f7f8df34b81e)

# OUTPUT
![Screenshot 2025-03-25 153446](https://github.com/user-attachments/assets/cd8b85f2-0f44-4d11-a8e2-d72b3b71ff2c)


# RESULT
Thus the program for creating a database using ORM hass been executed successfully
