# Local 3-Tier Deployment

Welcome to the "Local 3-Tier Deployment" project repository. This project guides you through the process of setting up and deploying a traditional 3-tier application on your Mac machine without using Docker. It serves as a foundational exercise before migrating to AWS and implementing DevOps practices.

## Project Overview

In this repository, we demonstrate the deployment of a 3-tier application locally:

1. **Web Tier**: This tier serves as the entry point for users and handles HTTP requests.
2. **Application Tier**: Here, the application logic is processed and communicates with the database tier.
3. **Database Tier**: This tier stores and manages application data.

## Getting Started

Follow these steps to set up and deploy the 3-tier application on your Mac without Docker:

### Prerequisites
- **check WIKI of detailed steps with snaps**: check prerequisites page [Prerequisites](https://github.com/mano444/Local-3Tier-Deployment/wiki/Prerequsistes)
for installation snaps of prereqs 

* Ensure you have the following software installed:

- **Java Development Kit (JDK)**: [Install JDK](https://www.oracle.com/java/technologies/javase-downloads.html)
- **Maven**: [Install Maven](https://maven.apache.org/install.html)
- **Application Server (e.g., Tomcat)**: [Install Tomcat](http://tomcat.apache.org/)
- **Database Server (e.g., MySQL)**: [Install MySQL](https://dev.mysql.com/downloads/installer/)

  
### CREATE Database, table and user on sql server and grant permissons to the user on database created based on requirments from sample_java repository 
- **CREATE DATABASE UserDB;
- **CREATE TABLE Employee ( id int unsigned auto_increment not null, first_name varchar(250), last_name varchar(250), email varchar(250), username varchar(250), password varchar(250), regdate timestamp, primary key (id) );
- **CREATE USER 'mano444'@'localhost' IDENTIFIED BY 'mano444'; (remeber these details to be provided for endpoint in java code) 
- **GRANT ALL PRIVILEGES ON UserDB TO 'mano444'@'localhost';


### Clone the Repository

git clone https://github.com/mano444/java_sample.git

###Prep before build##
-* update the application.properties file under src/main/resources/ with your database name and database user details created above 
-* create tomcat users  to deploy war file through browser itself 
--> cd /usr/local/bin/apache-tomcat-10.1.13/conf
---> nano tomcat-users.xml (create user and use it when deploying war through browser) 
--> cd /usr/local/bin/apache-tomcat-10.1.13/bin 
---> ./startup.sh ( starting tomcat) 



### Build and Run the Application


1. Navigate to the `java-app/` directory.

cd java-app/

2. Build the Java application artifact.

mvn clean install

3. Take war file created and Deploy the application to your application server (e.g., Tomcat).

4. Configure the application to connect to your database server (e.g., MySQL).


### Access the Application

Once the application is deployed and running, you can access it in your web browser:

# - Web Tier: http://localhost:8080

### Contributing

We welcome contributions, feedback, and collaboration. Feel free to explore and enhance this project.

 1. Fork the repository.
 2. Create your feature branch (`git checkout -b feature/your-feature`).
 3. Commit your changes (`git commit -m 'Add some feature'`).
 4. Push to the branch (`git push origin feature/your-feature`).
 5. Open a pull request.

