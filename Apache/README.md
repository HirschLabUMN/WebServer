# Apache webserver on redhat os
* Document root: /swadm/www
## General apache commands
* More commands and information can be found here: https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/5/html/deployment_guide/s1-apache-startstop
```bash
# Check your config files for syntax errors
apachectl configtest

# restart the server
sudo /sbin/service httpd restart
```

## Config and error log files
* Make sure to back up and configuration files before making any modifications. Similarly, make sure to alter the back up file names so they don't end with ".conf". Ending any backups with ".conf" will get picked up by apache and may cause errors.
* There are two seperate directories that house the configuration files. They are located at the following sites
```
# Main apache config file
/etc/httpd/conf/httpd.conf

# HTTPS/SSL config
/etc/httpd/conf.d/ssl.conf

# Django Web apps config
/etc/httpd/conf.d/django.conf

# apache module conf directory
/etc/httpd/conf.modules.d

# error log
/var/log/httpd/error_log
```
### https config file



### HTTPS information
* Important lines that were modified in the file
    * line120-130: set the path of the document root and allows access to dir
