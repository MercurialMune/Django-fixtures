##### DJANGO FIXTURES
A fixture for prepopulating your bikes model, for all bikes sold in Kenya. Granted, the list is not complete, so if you are with it, please contribute to add more makes and models

So you have a model like this?
```python
from django.db import models 
from django.contrib.postgres.fields import ArrayField

class Bikes(models.Model):
    make = models.CharField(max_length=100)
    model = ArrayField( models.CharField( max_length=100 ), blank=True )
```

Just store the ```bikes.json``` file in a folder named ```fixtures``` in your app directory.

Run ```./manage.py loaddata bikes.json``` in terminal to prepopulate your DB. Same goes for all other fixtures in this repo. You can contribute your own fixtures too.. 