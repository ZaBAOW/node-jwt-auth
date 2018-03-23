1) to sign up as a user:  
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

2) to retrieve a user token for password encryption
      - set the postman request to POST
      - append "api/auth/login" to url prefix
      - do steps 3-5 seen in step 1)
      enter your information into the text field
        ```
          {
            "username": <username>,
            "password": <password>
          }
        ```
      -press send to retrieve your user token
      
3) to access protected api endpoint
      - set Postman request to GET
      - append "api/protected" to url prefix
      - select the "Authorization" tab under the url
      - click the "Type" dropdown menu and select the "Bearer Token" option
      - copy/paste your api token into the "Token" field to the right
      - click send to access the endpoint
      
4) to refresh your auth token
      - set Postman request to POST
      - append "api/auth/refresh/" to url prefix
      - follow steps 3-5 in step e)
      - click send to recieve a new api token
