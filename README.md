# ts3_maintainer



Main repo for ts3 microservice application. 

# How to run
Normally we want to separate data storage layer and ts3 api service. So for production usage, you should start only part of the stack in docker-compose.
```
docker-compose up
```
#TODO: add credentials information
This should start the services needed, excluding ts3_query_http_api and databases. We assume that these parts shall be kept externally. 




# Architecture

1. ts3_query_http_api
This part is converting serverquery telnet calls into http rest api, so you can separate application logic and run it anywhere else. This part shall be served on the same server as your production teamspeak3 server resides.
2. ts3_maintainer (this repo)
Contains submodules to all other required microservices. It is created mainly for integration tests.
3. ts3_maintainer_service_channels (draft)
Business logic for maintaining channels. It uses ts3_query_http_api to perform operations on the ts3 server related to channels.

# Tests


:pig: to be filled

