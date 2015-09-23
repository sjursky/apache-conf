# apache-conf
Usefull Apache configurations, Proxy settings, hardening, ...

## Usage

Contains example configurations that can be included in main `httpd.conf` of Apache.

### Apache 2.2.26 on CentOS, Red Hat

Copy config files you like to Apache host (eg. `/etc/httpd/custom` directory) and include them with:

	Include custom/hardening.conf

**Hint:** Default Apache config already includes all `.conf` files from `conf.d/` directory. So just copy the ones that you like to `/etc/httpd/conf.d` and adjust to your needs.

## Contents

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