================
DINA-WEB : MediaServer-Demo
============

The MediaServer-Demo has been developed with the products below ( with those explicit in  versions).<br/>
Maven is used as the 'project management tool', Maven fetches all the dependencies that the Mediaserver relies on - each dependency is declared in the pom.xml-file.<br/>
OBS: before you 'mvn clean package' , you have to create a database+user&password ( grant access ) <br/>

## Launching
* Launch the mediaserver ( the ejb- & the resteasy-module )
* Launch the Demo ( the server & the client ) <br/>

## Testing  
1. request : fill in 'skata' in 'name'-field, blank in 'tags'-field
2. response : two images ( a flying 'pica pica' + a sitting 'pica pica' )

1. request : fill in 'skata' in 'name'-field, fill in 'view:flying'  in 'tags'-field
2. response : one image ( a flying 'pica pica' )

1. request : fill in 'skata' in 'name'-field, fill in 'view:sitting'  in 'tags'-field
2. response : one image ( a sitting  'pica pica' )

## Requirements
* Java SE 'Oracle Corporation': [JDK 1.7.0_51](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html)
* [Maven 3.0.5](http://maven.apache.org/download.cgi)
* [git client 1.9.1](http://git-scm.com/downloads)
* Application Server: [Glassfish 3.1.22](https://glassfish.java.net/downloads/3.1.2.2-final.html)
* Relational DBMS: [MySQL 5.5](http://dev.mysql.com/downloads/mysql/) or [PostgreSQL 9.1](http://www.postgresql.org/download/)
* and jdbc drivers [mysql-connector-java-5.1.23-bin.jar]() or [postgresql-9.1-901-1.jdbc4.jar]()

## Setup
* Make sure your [SSH
keys](https://help.github.com/articles/generating-ssh-keys) are set up
properly for GitHub.

## Clone
Clone the repository
```console
git clone https://github.com/Inkimar/dina-mediaserver-demo.git
cd dina-mediaserver-demo
```

### Operating system (Linux / Ubuntu)
[Ubuntu 14.04 LTS](http://www.ubuntu.com/download/desktop)
Kernel : 3.13.0-40-generic

### Additional configuration
The parent pom.xml resides in the 'DemoParentPom'-module. <br/>
All other modules fetch the java-version from that pom.xml


### Database
Use of [liquibase](http://www.liquibase.org/) which is a database-independent library for tracking, managing and applying database schema changes. <br/>
0. Create a database+user in your preferred db <br/>

<b>MySQL or PostgreSQL</b> <br/>
Configuration of chosen RDBMS affects the following modules/files: <br/>
1. <b>Module 'Mediaserver-database-management'</b> <br/>
1.1 liquibase.properties <br/>
2. <b>Module 'MediaserverApp-ejb'</b> <br/>
2.1 glassfish-resources.xml <br/>
2.2 persistence.xml <br/>
3 drop respective <database>-jdbc-jar into 'glassfish/.../lib-library' 




### IDE used in development
[Netbeans 8.x](https://netbeans.org/downloads/) 
