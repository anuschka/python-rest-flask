# Flask Rest API

This code is a self explanatory code, I got from [here](https://www.codementor.io/sagaragarwal94/building-a-basic-restful-api-in-python-58k02xsiq). 

The current repository helps in getting started with the basic REST API Development in Flask. The sole existence of this repo is for a [Powercoders lecture](http://powercoders.org/). The application uses [chinook.db](http://www.sqlitetutorial.net/sqlite-sample-database/) that students used in the SQL workshop.

## Prerequisites
+ a computer with Python installed
+ virtual environment (which is a copy of the Python interpreter onto which you can install packages privately, without affecting the global Python interpreter installed in your system)

### Virtual Environment
+ on Python 3: 
```python
python3 -m venv virtual-environment-name
```
+ on Python 2:
```python
sudo pip install virtualenv
```
+ to start using a virtual environment, you have to “activate” it:
```python
source venv/bin/activate
```

## Run the code

+ Clone this repository.
```python
git clone https://github.com/anuschka/python-rest-flask.git
```
+ cd into python-rest-flask
+ Install the requirements
```python
pip install -r requirements.txt
```
+ Setup environment variables
```python
FLASK_APP=app.py
FLASK_DEBUG=True
```
+ Run Flask
```python
flask run
```

## Test the code
There are three endpoints in the application:

+ http://127.0.0.1:5002/employees shows ids of all the employees in database
+ http://127.0.0.1:5002/tracks shows tracks details
+ http://127.0.0.1:5002/employees/8 shows details of employee whose employee ID is 8

To create a new record in the Employees table:
```python
curl -H "Content-Type: application/json" -X POST -d '{"LastName":"Power","FirstName":"Coder","Title":"Developer","ReportsTo":"Matthias","BirthDate":"1.1.1990","HireDate":"20.9.2017","Address":"GarageHub","City":"Zurich","Country":"Switzerland","State":"None","PostalCode":"8100","Phone":"0123456789","Fax":"0123456789","Email":"coder@powercoders.com"}' http://127.0.0.1:5000/employees
```

To delete Employee whose employee ID is 8:
```python
curl -H "Content-Type: application/json" -X DELETE -v http://127.0.0.1:5000/employees/8
```











