# 📘 Day 04: Running MariaDB in Docker

This lab focuses on deploying MariaDB within a Docker container, emphasizing containerization and data persistence.

## 🔍 Lab Details

- **Module:** Learn By Doing - MariaDB
- **Lesson:** [MariaDB on Docker](https://learn.kodekloud.com/user/courses/learn-by-doing-mariadb/module/d87e82ef-bbc1-451a-aac9-6cfd75d0c981/lesson/2cc81dcf-6b49-46d7-9b9b-4b8ce74310ab)

## 🛠️ Skills Practiced

- Deploying MariaDB using Docker containers
- Configuring persistent storage for data durability
- Managing MariaDB instances within a containerized environment

## 💻 Commands Used

```bash
# Pull the MariaDB image
docker pull mariadb

# Run MariaDB container with environment variables and volume mapping
docker run --name mariadb-container -e MYSQL_ROOT_PASSWORD=my-secret-pw -v /my/own/datadir:/var/lib/mysql -d mariadb

# Verify the container is running
docker ps

# Access the MariaDB shell inside the container
docker exec -it mariadb-container mysql -u root -p
