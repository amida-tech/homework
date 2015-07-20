# Amida Homework
Programming exersize for new dev team candidates



## 1 - Parsing data

Write parser that convert CMS Blue Button data file (ascii format) into JSON.
Sample file - `parse/cms_sample.txt`.

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

Create basic API. It should run as standalone HTTP server.

HTTP GET request to `http://localhost:4000/api/hello` should return following JSON structure with 200 OK HTTP code:

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

Using provided HTML file `frontend/index.html` implement date validation using pure JavaScript (e.g. no jQuery or other JS frameworks).

On clicking "validate" button, `<p id="validation"></>` element should be populated either with "Valid Date" message or "Invalid Date: <some desctiption of the problem>".


### Last updated
July 20, 2015