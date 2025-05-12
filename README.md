HelloWorld Servlet example with corresponding Dockerfile

Use Maven Build first to create war file in Target folder.

mvn clean package

Artifact will be created in target folder.

docker build -t mavenbuild .

Once this is done u will be see image using docker image

Use below command to run the container

docker run -d -p 8080:8080 --name dockercontainer mavenbuild

Not following these. INstead,
running maven via worflow to build a .WAR file. then invoking a jenkins pipeline from the github workflow
jenkins will then deploy to tomcat
