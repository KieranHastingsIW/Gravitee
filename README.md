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
 - While using the httpbin.org backend we should see a JSON file returned with the headers sent by the request in the headers of the returned text.
 



