"# py2018"

from flask_wtf import FlaskForm
ывапытпываптоывапыр


class ShowReservationsOnDateForm(Form):
    reservation_date = DateField('reservation_date', default=datetime.now())

class AddTableForm(Form):
    table_capacity = SelectField('table_capacity', coerce=int, choices = [(x, x) for x in range(1, MAX_TABLE_CAPACITY)]) 
