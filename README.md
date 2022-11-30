# Gravitee
A repo to practice the use and implementation of the Gravitee API management platform and includes installation and testing for deployment of Gravitee within a Docker container.  

# Instillation process
    NOTE: These instruction assume you already have docker and docker for desktop installed on the system you are wanting to be your host and that docker desktop is running. 
    
 1. In your CLI cd to the directory you wish to run the compose file from.
 2. Clone this repo to your directory of choice.
 3. cd into the newly created file.
 4. Run the compose command 'docker compose up'
 5. In docker desktop confirm that all 6 containers are running, they should be named as follows (unless redefined by yourself).
    - gio_apim_mongodb
    - gio_apim_elasticsearch
    - gio_apim_gateway
    - gio_apim_management_ui
    - gio_apim_management_api
    - gio_apim_portal_ui
 6. By default the Gravitee APIM console will be ported to port 8084, to access this in your search engine of choice look up 'localhost:8084'.
   - In this console Publishers are able to publish APIs and Admins can configure global platform settings and specific portal settings 
 7. In the console select the APIs tab (the collection of rectangles in the nav bar on the right-hand side of the screen, below the home tab)
 8. Select "+ Add Api", then "Continue in the wizard" 
 9. Name your API, give it a description and Version number, and define the context path, this is where the API will be reachable.
 10. For this example we will use the httpbin.org/anything backend for testing purposes. Set the Backend to 'https://httpbin.org/anything'.
 11. Create and name a plan that has the keyless security type 
 12. skip the next step, then when prompted select "CREATE AND START THE API" 
13. To check if the backend, the path, and the Gravitee API manager as a whole has been set up correctly so far in your search engine of choice search 'localhost:8082/{enter your /pathname here}'
 - While using the httpbin.org backend we should see a JSON file returned. Its content should be simular to as follows.

 {
  "args": {}, 
  "data": "", 
  "files": {}, 
  "form": {}, 
  "headers": {
    "Accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9", 
    "Accept-Encoding": "deflate, gzip", 
    "Accept-Language": "en-US,en;q=0.9", 
    "Cookie": "WMF-Last-Access=28-Nov-2022; Auth-Graviteeio-APIM=Bearer%20eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI2YWIyOGYzMi1mODU5LTRhNjAtYjI4Zi0zMmY4NTkxYTYwMjciLCJwZXJtaXNzaW9ucyI6W3siYXV0aG9yaXR5IjoiRU5WSVJPTk1FTlQ6QURNSU4ifSx7ImF1dGhvcml0eSI6Ik9SR0FOSVpBVElPTjpBRE1JTiJ9LHsiYXV0aG9yaXR5IjoiT1JHQU5JWkFUSU9OOkFETUlOIn0seyJhdXRob3JpdHkiOiJPUkdBTklaQVRJT046VVNFUiJ9LHsiYXV0aG9yaXR5IjoiRU5WSVJPTk1FTlQ6QURNSU4ifSx7ImF1dGhvcml0eSI6IkVOVklST05NRU5UOlVTRVIifV0sImlzcyI6ImdyYXZpdGVlLW1hbmFnZW1lbnQtYXV0aCIsImV4cCI6MTY3MDM1NTExMCwiaWF0IjoxNjY5NzUwMzEwLCJqdGkiOiJlZjM1OTBmZi02NWZkLTRmMTQtYjQ4Yi0yNjRhZGYzZjVmYTEifQ.Z2gbsqwTN-k36-yyPlup24fquK4Xneqxqq6VyhCwtMY; XSRF-TOKEN=eyJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJncmF2aXRlZS1tYW5hZ2VtZW50LWF1dGgiLCJpYXQiOjE2Njk3NzE0NzMsInRva2VuIjoiY2ZjMjdjMjktMzM4MC00YTdiLThkMzItNmQ1NWFmNjBiNDgxIn0.ZFcd25P6S76uQD4rAJBJQMyA50svo4wdW1NL645-65M", 
    "Host": "httpbin.org", 
    "Sec-Ch-Ua": "\"Google Chrome\";v=\"107\", \"Chromium\";v=\"107\", \"Not=A?Brand\";v=\"24\"", 
    "Sec-Ch-Ua-Mobile": "?0", 
    "Sec-Ch-Ua-Platform": "\"Windows\"", 
    "Sec-Fetch-Dest": "document", 
    "Sec-Fetch-Mode": "navigate", 
    "Sec-Fetch-Site": "none", 
    "Sec-Fetch-User": "?1", 
    "Upgrade-Insecure-Requests": "1", 
    "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/107.0.0.0 Safari/537.36", 
    "X-Amzn-Trace-Id": "Root=1-6386b0de-19f16c1209c9182055f7a288", 
    "X-Gravitee-Request-Id": "9707a61a-d160-465d-87a6-1ad160e65dff", 
    "X-Gravitee-Transaction-Id": "9707a61a-d160-465d-87a6-1ad160e65dff"
  }, 
  "json": null, 
  "method": "GET", 
  "origin": "203.86.192.144", 
  "url": "https://httpbin.org/anything"
}
 



