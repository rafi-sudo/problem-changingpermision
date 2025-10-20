Sure! Here's the same document translated into English Markdown:

# Troubleshooting Icecast2 & Lighttpd: Permissions and Service Restart

This document explains the steps to fix issues when restarting the `icecast2` or `lighttpd` services related to directory permissions.

---

## 1. Icecast2 Issues

When trying to restart Icecast2 with:

```bash
sudo /etc/init.d/icecast2 restart

You may see output like:

[....] Restarting icecast2 (via systemctl): icecast2.se[ ok .

If the service does not run properly or there are permission errors, follow these steps.

1.1 Check and fix directory ownership

# Change ownership of configuration and log directories
sudo chown -R icecast2:icecast /etc/icecast2
sudo chown -R icecast2:icecast /var/log/icecast2

1.2 Check and fix directory permissions

sudo chmod -R 755 /var/log/icecast2

1.3 Restart the Icecast2 service

sudo systemctl restart icecast2
sudo systemctl status icecast2

If active (running) appears, the service is running normally.


---

2. Lighttpd Issues

For Lighttpd, common problems are related to permissions on the log, cache, and run directories.

2.1 Check and fix directory ownership

sudo chown -R www-data:www-data /var/log/lighttpd
sudo chown -R www-data:www-data /var/cache/lighttpd
sudo chown -R www-data:www-data /var/run/lighttpd

2.2 Check and fix directory permissions

sudo chmod -R 750 /var/log/lighttpd
sudo chmod -R 750 /var/cache/lighttpd
sudo chmod -R 750 /var/run/lighttpd

2.3 Restart the Lighttpd service

sudo systemctl restart lighttpd
sudo systemctl status lighttpd

Make sure active (running) appears.


---

3. Additional Notes

Always check the user running the service (icecast2 for Icecast2, www-data for Lighttpd).

Incorrect directory permissions are a common cause of services failing to start.

Only change ownership and permissions for service-related directories—avoid modifying root /.



---

This document is intended to simplify troubleshooting Icecast2 and Lighttpd on Linux servers (Debian/Armbian).

If you want, I can also make a **compact copy-paste version** for English that you can just run in the terminal without extra reading. Do you want me to do that?

