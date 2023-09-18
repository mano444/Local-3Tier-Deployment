# Local-3Tier-Deployment
Welcome to the "Local 3-Tier Deployment" project repository. This repository serves as a practical starting point for deploying a simple 3-tier application on your Mac machine. The project provides insights into the architecture and deployment process before transitioning to AWS and embracing DevOps practices.

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

Ensure you have the following software installed:

- **Java Development Kit (JDK)**: [Install JDK](https://www.oracle.com/java/technologies/javase-downloads.html)
- **Maven**: [Install Maven](https://maven.apache.org/install.html)
- **Application Server (e.g., Tomcat)**: [Install Tomcat](http://tomcat.apache.org/)
- **Database Server (e.g., MySQL)**: [Install MySQL](https://dev.mysql.com/downloads/installer/)

### Clone the Repository

```shell
git clone https://github.com/your-username/Local-3Tier-Deployment.git
cd Local-3Tier-Deployment


### Build and Run the Application

```shell
1. Navigate to the `java-app/` directory.

cd java-app/

2. Build the Java application artifact.

mvn clean install

3. Deploy the application to your application server (e.g., Tomcat).

4. Configure the application to connect to your database server (e.g., MySQL).
### Access the Application

# Once the application is deployed and running, you can access it in your web browser:

# - Web Tier: http://localhost:8080

### Contributing

# We welcome contributions, feedback, and collaboration. Feel free to explore and enhance this project.

# 1. Fork the repository.
# 2. Create your feature branch (`git checkout -b feature/your-feature`).
# 3. Commit your changes (`git commit -m 'Add some feature'`).
# 4. Push to the branch (`git push origin feature/your-feature`).
# 5. Open a pull request.

