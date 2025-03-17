# Important Log Sources  
Ensure the following log sources are active and the related files are created in the specified paths. Periodically back up these logs on a separate system.  

| Log Sources | Description |
|-------------|-------------|
| /var/log/auth.log | Logs related to authentication and system login |
| /var/log/syslog | General system logs |
| /var/log/kern.log | Kernel-related logs |
| /var/log/dmesg | Logs related to system boot |
| /var/log/apt/history.log | Logs related to software package installation and removal |
| /var/log/ufw.log | Logs related to the UFW firewall |
| /var/log/apache2/access.log | Apache server access logs |
| /var/log/apache2/error.log | Apache server error logs |
| /var/log/mysql/error.log | MySQL error logs |
| /var/log/postgresql/postgresql.log | PostgreSQL logs |
| /var/log/cron | Logs related to scheduled tasks (Cron Jobs) |
| /var/log/maillog | Logs related to emails |
| /var/log/audit/audit.log | Logs related to Auditd |
