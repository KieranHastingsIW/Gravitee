# Gravitee
A repo to practice the use and implementation of the Gravitee API management platform and includes instilation and testing for deployment of gravitee within a Docker container.  

# Instilation process - in comand line 
    NOTE: These instruction assume you already have docekr and docker for desktop installed on the system you are wanting to be your host and that docker desktop is running. 
    PS. The curl command used in these instructions seems to not work in powershell. 
 1. In your search engine of choice look up 'https://www.gravitee.io/downloads'
 2. Scroll untill you see the Download API management section, select Docker and copy the command.
 3. In you command line interface direct yourself to the location you would like the compose file to be located and run the copied command.
 4. Once the compose file has downloaded run the compose comand 'docker compose up'
 5. In docker desktop confirm that all 6 containers are running, the should be named as follows (unless redefined by yourself).
    - gio_apim_mongodb
    - gio_apim_elasticsearch
    - gio_apim_gateway
    - gio_apim_management_ui
    - gio_apim_management_api
    - gio_apim_portal_ui
 6. By default the gravitee APIM console will be ported to port 8084, to access this in your search engine of choice look up 'localhost:8084'.
 7. image.png


