# namaste
Microservice using Dropwizard

Build and Deploy namaste
--------------------

1. Open a command prompt and navigate to the root directory of this microservice.
2. Build the executable jar file:

        mvn clean package

3. Execute the jar file:

        java -jar target/namaste.jar

Access the application
----------------------

The application will be running at the following URL: <http://localhost:8080/api/namaste>


## Deploy in Openshift

1. In CDK directory, export the environment variables to have access to Docker daemon

		eval "$(vagrant service-manager env docker)"

2. Type this command to build and deploy the microservice in Openshift/CDK

		mvn clean package docker:build fabric8:json fabric8:apply