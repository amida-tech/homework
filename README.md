# Amida Homework
Programming exercise for new dev team candidates.

## Part 1: Parsing Data

Write a parser that converts a Blue Button CMS data file (ASCII format) into JSON.

* Sample file: [parse/cms_sample.txt](./parse/cms_sample.txt). 
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

## Part 2: API

Create a basic REST API to serve content via HTTP GET requests.

* Sample file: [api/sample.json](./api/sample.json).
* The API should run as a standalone HTTP server.
* An HTTP GET request to `http://localhost:4000/api/sample` should return the following JSON structure with a 200 OK HTTP code:

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

## Part 3: Ingest and Parse Data

Implement a simple page to allow HTTP POST.

Using your existing HTTP server, add a route to POST data to `http://localhost:4000/api/parse`.
The route should take a CMS `.txt` file (from part 1) as a payload, and should then parse the file
(using your parser), saving the resultant JSON to `post.json`.

Create a simple webpage, using any framework(s) of your chosing, to allow a user to pick
a file and POST it to your HTTP server.

* Include instructions for running both the client and server. They should run as separate services.
* The POST should return 200 if the parsing was successful; otherwise, return some sort of error.
* You may display the returned HTTP code and error information on your webpage, if you wish.


### Last updated
October 5, 2016
