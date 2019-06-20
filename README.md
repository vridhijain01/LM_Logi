# LM_Logi
This is a Maven project which includes following features.

 - Logistics API testing
 - Place order API
 - Fetch order details API
 - Driver to Take the Order API
 - Driver to Complete the Order API
 - Cancel Order API

How to run
-------------
 - Clone the repository
 - Make sure you are using JDK 1.8 and Maven 
 - Open Project 
 - Make sure docker is running on the system
 - Run following docker commands:
 - $ docker network create lalamove-sample-api || true
 - $ docker rm -f lalamove-sample-api-db
 - $ docker run -d --net=lalamove-sample-api --name lalamove-sample-api-db lalamove/lalamove-sample-api-db:1.0
 - $ docker rm -f lalamove-sample-api
 - $ docker run -d --net=lalamove-sample-api --name lalamove-sample-api -p 51544:8000 lalamove/lalamove-sample-api:1.0
 - $ curl -X GET -H "Content-Type: application/json; charset=utf-8" http://localhost:51544/ping
