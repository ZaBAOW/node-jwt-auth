# Project Title

JWT authentication tests for furthering my understanding of how JWT authentication works, as well as the process of creating a JWT for a user
for the purpose of safegaurding the user's critical information(i.e. password).

## Getting Started

Begin by either:
  1) cloning the "node-jwt-auth" repository to your local device ("https://github.com/Thinkful-Ed/node-jwt-auth/")
  2) remixing the glitch at ("https://glitch.com/edit/#!/feather-pizza")
  
Steps if you cloned github repository:  
  1) you will need to install 3 pieces of software:  
    a) [gitbash](https://gitforwindows.org/)  
    b) [Postman](https://www.getpostman.com/)  
    c) [Mongo](https://www.mongodb.com/download-center#community)  
  2)open 2 seperate git bash windows  
    a)window one:  
      - type cd to move to general directory
      - type mongod to initiate the server
    b)window two:  
      - locate the directory you cloned your version of the repository into
      - type "npm test" to make sure there are no issues with the code
      - type "npm start" to start up the local server
  3) open Postman  
    a) create a new postman session  
    b) for the url prefix input "http://localhost:8080/"  
    c) to sign up as a user:  
      - set the postman request to POST
      - append "api/users" onto the end of your url prefix
      - click on the "body" tab underneath the url
      - select the "raw" bubble
      - click on the dropdown menu to the right of the bubble selection and select the JSON format
      - enter your infomation into the text field
        ```
            {
              "username": <username>,
              "password": <password>,
              "firstName": <yourFirstName>,
              "lastName": <yourLastName>
            }
        ```
      - press "send" to send the request
    d) to retrieve a user token for password encryption
      - set the postman request to POST
      - append "api/auth/login" to url prefix
      - do steps 3-5 seen in step c)
      enter your information into the text field
      ```
          {
            "username": <username>,
            "password": <password>
          }
      ```
      -press send to retrieve your user token
    e) to access protected api endpoint
      - set Postman request to GET
      - append "api/protected" to url prefix
      - select the "Authorization" tab under the url
      - click the "Type" dropdown menu and select the "Bearer Token" option
      - copy/paste your api token into the "Token" field to the right
      - click send to access the endpoint
    f) to refresh your auth token
      - set Postman request to POST
      - append "api/auth/refresh/" to url prefix
      - follow steps 3-5 in step e)
      - click send to recieve a new api token
  

### Prerequisites

to do

```
Give examples
```

### Installing

A step by step series of examples that tell you have to get a development env running

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```

```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

to do

## Contributing

Andrew Kadesky (no contributors)

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags).

## Authors
Andrew Kadesky

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone who's code was used
* Inspiration
* etc
