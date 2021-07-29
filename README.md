![Open Source Love](https://img.shields.io/badge/Open%20%E2%9D%A4%EF%B8%8FSource-blue)


** Creating Virtual Environment for Python API **
-- python3 -m venv .venv
source .venv/bin/activate

This will be isolate the dependecies for specific application.
pip3 install flask
pip3 install flask-sqlalchemy

Create dependecies file
pip3 freeze > requirements.txt

(.venv) pporras@pporrasxumak api % export FLASK_APP=application.py
(.venv) pporras@pporrasxumak api % export FLASK_ENV=development

to run this app need to create this Environment variables

Create MODEL
From the python3 terminal run:

from application import db

Create db structure
db.create_all()

Create objects in DB
from application import Drink
drink = Drink(name="Grape Soda", description="Taste like grapes")
drink
db.session.add(drink)
db.session.commit()

>>> drink = Drink(name="Orange Soda", description="Taste Like Orages")
>>> drink = Drink(name="Orange Soda", description="Taste Like Oranges ")
>>> drink2 = Drink(name="Cola Soda", description="Taste Like Cola")
db.session.add(Drink(name="Root Beer", description="Tastes like root beer"))
>>> db.session.add(drink,drink2)
>>> db.session.commit()
>>> Drink.query.all()



