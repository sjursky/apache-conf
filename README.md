# apache-conf
Usefull Apache configurations, Proxy settings, hardening, ...

## Contents

Contains example configurations that can be included in main `httpd.conf` of Apache

### encoding.conf

Configuration if you want to handle URI decoding by background application

### hardening.conf

Minimum hardening of Apache server to not leak information like:

- Server version
- inodes
- MIME-sniffing

And to prevent some basic hack attacks like:

- anti-clickjacking
- XST
- DOS by posting big payloads

### proxy-tomcat.conf

Sample configuration of Tomcat AJP proxy by balancer

### proxy-weblogic.conf

Sample configuration of WebLogic proxy with URI encoding suggestions

### static.conf

Configuration for static files that resides on Apache.
Includes: 

- `Cache-Control` headers config for different file types
- `gzip`-ing of responses to lower traffic bandwidth

### status.conf

Configuration of server status page. This is needed if you plan to monitor Apache with tools like Zabbix.