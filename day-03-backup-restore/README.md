# 📘 Day 03: MariaDB Backup and Restore

This lab focuses on performing full backups and restores in MariaDB using the `mariadb-backup` tool.

## 🔍 Lab Details

- **Module:** Learn By Doing - MariaDB
- **Lesson:** [Backup and Restore](https://learn.kodekloud.com/user/courses/learn-by-doing-mariadb/module/d87e82ef-bbc1-451a-aac9-6cfd75d0c981/lesson/e73f60c4-73ef-44aa-aedf-b47ee83debbd)

## 🛠️ Skills Practiced

- Performing full backups using `mariadb-backup`
- Preparing backups for restoration
- Restoring data using `--copy-back` and `--move-back` options
- Managing file permissions post-restore

## 💻 Commands Used

```bash
# Backup the database
mariadb-backup --backup --target-dir=/var/mariadb/backup/ --user=mariadb-backup --password=mypassword

# Prepare the backup
mariadb-backup --prepare --target-dir=/var/mariadb/backup/

# Stop MariaDB service
systemctl stop mariadb

# Restore the backup
mariadb-backup --copy-back --target-dir=/var/mariadb/backup/

# Adjust ownership
chown -R mysql:mysql /var/lib/mysql/

# Start MariaDB service
systemctl start mariadb
