# VProfile DevOps Project

## Overview

VProfile is a Java-based web application project using a multi-tier technology stack. This repository documents the application's core technologies, prerequisites, and database setup.

The project provides an opportunity to explore Java web application deployment and the supporting services commonly used in application environments.

## Technology Stack

- **Backend:** Java, Spring MVC, Spring Security, Spring Data JPA
- **Build Tool:** Maven
- **Frontend:** JSP
- **Application Server:** Apache Tomcat
- **Database:** MySQL 8
- **Caching:** Memcached
- **Messaging:** RabbitMQ
- **Search:** Elasticsearch

## Prerequisites

Install the following software before setting up the project:

- JDK 11
- Maven 3
- MySQL 8

You may also need the appropriate versions of Tomcat, Memcached, RabbitMQ, and Elasticsearch, depending on the project's configuration.

## Database Setup

The repository includes a MySQL database dump:

`src/main/resources/db_backup.sql`

### Import the database

1. Ensure MySQL is installed and running.
2. Create the database named `accounts` if it does not already exist.
3. From the directory containing the SQL dump, import the database using:

```bash
mysql -u <user_name> -p accounts < src/main/resources/db_backup.sql
```

Replace `<user_name>` with your MySQL username. Enter your password when prompted.

If you run the command from the directory containing `db_backup.sql`, use:

```bash
mysql -u <user_name> -p accounts < db_backup.sql
```

## Build and Deployment

JDK 11 and Maven 3 are listed as project prerequisites. Before building or deploying the application, review the project's Maven configuration and application settings to confirm the required versions, service endpoints, credentials, and deployment procedure.

Use the deployment instructions and configuration files included in the repository as the source of truth for the environment-specific setup.

## Notes

- Keep database credentials and other secrets out of version control.
- Confirm that MySQL, Memcached, RabbitMQ, and Elasticsearch are configured as required by the application.
- Verify the application's configuration before deploying it to a new environment.

## License

Refer to the repository's license file, if present, for usage and distribution terms.
