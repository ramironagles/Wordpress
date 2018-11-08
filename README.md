# Wordpress + AppDynamics + Docker

Example of how to add AppDynamics PHP Agent to a Wordpress Apache container

## Getting Started
* [AppDynamics](https://download.appdynamics.com) - Download and rename the PHP agent to 
```
appdynamics.tar.bz2
```

Set the AppDynamics values, in docker-compose.yml. (Account, Tier, Application, Access Key, Controller, Controller Port)

If you want to change nodename, /usr/local/bin/docker-entrypoint.sh script. By default it will set the AppDynamics Node name to the first 12 characters of the containerid.

Build image docker build -t appd-php:latest .

Run Example: docker-compose up -d

If you need to inspect the logs, they will be located in /opt/appdynamics/php-agent/logr
