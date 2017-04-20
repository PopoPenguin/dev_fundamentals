Tomcat Deployment
====

Apache Tomcat is used to deploy your Java Servlets and JSPs. So in your Java project you can build your WAR (short for 
Web ARchive) file, and just drop it in the deploy directory in Tomcat. So basically Apache is an HTTP Server, serving HTTP. 
Tomcat is a Servlet and JSP Server serving Java technologies.

Installing
----

http://tomcat.apache.org/

Tomcat 8
> * `sudo yum install tomcat8-webapps tomcat8-admin-webapps`


Tomcat 9
> * `sudo yum install tomcat9-webapps tomcat8-admin-webapps`

Start
> * `sudo service start tomcat<version> start`

Stop
> * `sudo service start tomcat<version> stop`


Adding admin users to manage apps via {host}:8080/manager/html
> * vim <tomcat_dir>/conf/tomcat-users.xml
> * add the following to the bottom of the file just above the </tomcat-users> tag:
`<role rolename="manager-gui"/>
   <user username="admin" password="admin" roles="manager-gui"/>`


Deploying your applications
----

You have two options:
> * Deploy your apps using the GUI (Manager App) {host}:8080/manager/html

or

> * Copy your war file into the "webapps" folder of the tomcat installation. After copying your .war file into the 
webapps directory your .war will be unpacked and deployed automatically


