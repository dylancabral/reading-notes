## In your own words, describe what each group of status code represents:

100’s = 100 level codes are informational status codes, tell the client that a request hsa been recieved and will try to comply
200’s = success codes, or okay codes, it meant it met all validation the time of sending
300’s = redirection codes, they tell you that the locatuion you are requesting from doesnt have the details you need and will tell you to request to the updated location
400’s = client error codes they are for invalid requests to a server from a client, a client is sending incorrect input and should reevaluate the perameters
500’s = server error codes, indicate problems with an overwhelkmed server or unreachable servers hidden behind a proxy 
## What is a status code 202?
this is an a accepted code, asynchronus processing, code tells the client that the request was valid but its processing will be finished in the future
## What is a status code 308?
this tells the client to use another url to access the RESOURCE and not to use the current url anylonger
## What code would you use if an update didn’t return data to a client?
a 204 code shows no content was returned
## What code would you use if a resource used to exist but no longer does? 
410 error code shows is like a 404 but the resource has existed in the past but we dont know where it went 
## What is the ‘Forbidden’ status code?
403 the client has authorized or doesnt need to authorize itself, but still has no permissions to access the resource

## Why do we need to pull our MongoDB database string out of our server and put it into our .env?
this way it pulls from our env location rather than our local server
## What is middleware?
middle ware is code that runs before it gets passed to your routes basically translates the code for us
## What does app.use(express.json()) do?
implements the information in json format so that it can be read and processed according to the json express traits

## What does the /:id mean in a route?
it means it is a paramater and can be acccessed through .params
## What is the difference between PUT and PATCH?
patch updates based on what the user passes us rather than put which updates all of the information about the subscriber or user all at once 
## How do you make a default value in a schema?
default.now()
## What does a 500 error status code mean?
means that there is an error on our server it is entirely a fault of the server we created not the user or the resource 

## What is the difference between a status 200 and a status 201?
201 means successfully created an object 
200 means everything was successful, just less specific
