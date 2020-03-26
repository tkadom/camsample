# Workflow Application Prototype #
Ongling work around prototyping a camunda workflow with spring boot
## Camunda ##
Great place to get started with Camunda is here:
https://camunda.com/bpmn/examples/

## Pre-requisites ##
In order to run this software, you will need to have a java development environment in place that includes a JDK, Maven, and Docker

* Install Java (currently should work with everything post Java 8)
* Install Maven
* Install Docker

## build ##
from directory with pom.xml file
* mvn install

## Run Application: ##
The application currently has a web, and a database container.  For the database, a database initialization script is built off camunda 7.12 schema files.  Camunda corresponding SQL source is checked in under scripts.  If there are errors in the application related to the database, check with Camunda for updates to the database schema or ensure that you are locked at version 7.12. 

* docker-compose up -d --build

## Stop the flow ##
* docker-compose stop

## Access Application: ##
The docker compose will map the web instance port 8080 to localhost 8090.  so it can be accessed by:
http://localhost:8090/kadom-1.0.0
* login with
	* username admin/admin


## Next Steps ##
Auto Deployment from github TBD

##Install GoCD:
docker-compose up -d
