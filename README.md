# Amida Homework
Programming exercise for new dev team candidates



## 1 - Parsing data

Write a parser that converts a CMS Blue Button data file (ASCII format) into JSON.
Sample file - `parse/cms_sample.txt`. You only need to parse the "Demographics" section of the file.

Output format:

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

Create a basic API. It should run as a standalone HTTP server.

An HTTP GET request to `http://localhost:4000/api/hello` should return the following JSON structure with a 200 OK HTTP code:

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

Using provided HTML file `frontend/index.html` implement date validation using pure JavaScript (e.g. no jQuery or other JS frameworks). Date should be entered in "MM/DD/YYYY" format; assume for the purpose of this exercise that all years are leap years (e.g. February 29 is a valid date).

On clicking the "validate" button, `<p id="validation"></>` element should be populated either with "Valid Date" message or "Invalid Date: <some description of the problem>".


### Last updated
July 20, 2015
