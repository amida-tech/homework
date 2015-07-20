# Amida Homework
Programming exercise for new dev team candidates



## 1 - Parsing data

Write a parser that converts a CMS Blue Button data file (ASCII format) into JSON.

* Sample file - [parse/cms_sample.txt](./parse/cms_sample.txt). 
* You only need to parse the "Demographics" section of the file.
* The parser should return data in the following format:

```
{
    "name": {
        "first_name": "JOHN",
        "last_name": "DOE"
    },
    "dob": "01/01/1910",
    "address": ["123 ANY ROAD"],
    "city": "ANYTOWN",
    "state": "VA",
    "zip": "00001",
    "phone": "123-456-7890",
    "email": "johndoe@example.com",
    "coverage": [{
        "type": "Part A",
        "effective_date": "01/01/2012"
    }, {
        "type": "Part B",
        "effective_date": "01/01/2012"
    }]
}
```

## 2 - Backend API

Create a basic API.

* Sample file - [api/sample.json](./api/sample.json)
* The API should run as a standalone HTTP server
* An HTTP GET request to `http://localhost:4000/api/hello` should return the following JSON structure with a 200 OK HTTP code:

```
{
    "data": {
    	//content of api/sample.json file goes here
    },
    "metadata": {
        "generated": "07/20/2015 10:49AM" //current date and time
    }
}
```

## 3 - Frontend validation

Implement date validation using pure JavaScript.


* Sample file - [frontend/index.html](./frontend/index.html)
* Use pure JavaScript (e.g. no jQuery or other JS frameworks)
* Dates should be entered in "MM/DD/YYYY" format
* Assume for the purpose of this exercise that all years are leap years (e.g. February 29 is a valid date)
* Dates in the future are valid
* On clicking the "validate" button, the `<p id="validation"></>` element should be populated either with a "Valid Date" message or "Invalid Date: <some description of the problem>"



### Last updated
July 20, 2015
