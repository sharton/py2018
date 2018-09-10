"# py2018"

from flask_wtf import FlaskForm
from wtforms import StringField, DateTimeField, IntegerField, DateField, SelectField
from wtforms.validators import DataRequired
from .models import MAX_TABLE_CAPACITY

from datetime import datetime




class ShowReservationsOnDateForm(Form):
    reservation_date = DateField('reservation_date', default=datetime.now())

class AddTableForm(Form):
    table_capacity = SelectField('table_capacity', coerce=int, choices = [(x, x) for x in range(1, MAX_TABLE_CAPACITY)]) 
