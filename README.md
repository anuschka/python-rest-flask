# Flask Rest API

This code is a self explanatory code, I got from [here](https://www.codementor.io/sagaragarwal94/building-a-basic-restful-api-in-python-58k02xsiq) blog. 

The current repository, helps in getting started with the basic REST API Development in Flask. The sole existence of this repo is for a [Powercoders lecture](http://powercoders.org/). The application uses [chinook.db]()http://www.sqlitetutorial.net/sqlite-sample-database/ that students used in the SQL workshop.

# Prerequisites

Python and virtual environment.

# Run the code

Clone this repository.
Install the requirements.
Setup environment variables.
Run Flask.

# Test the code
There are three endpoints in the application:

+ http://127.0.0.1:5002/employees shows ids of all the employees in database
+ http://127.0.0.1:5002/tracks shows tracks details
+ http://127.0.0.1:5002/employees/8 shows details of employee whose employee ID is 8

To create a new record in the Employees table:
```curl -H "Content-Type: application/json" -X POST -d '{"LastName":"Power","FirstName":"Coder","Title":"Developer","ReportsTo":"Matthias","BirthDate":"1.1.1990","HireDate":"20.9.2017","Address":"GarageHub","City":"Zurich","Country":"Switzerland","State":"None","PostalCode":"8100","Phone":"0123456789","Fax":"0123456789","Email":"coder@powercoders.com"}' http://127.0.0.1:5000/employees```

To delete Employee whose employee ID is 8:
```curl -H "Content-Type: application/json" -X DELETE -v http://127.0.0.1:5000/employees/8```











