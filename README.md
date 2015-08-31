Introduction
----

This repo contains some Docker Compose configuration files which let you fire up CJP services in various ways.

Available configurations
* `cjoc-two-masters.yml` - This is CJOC with two CJE masters. Some assembly required. 
  Once complete, CJOC will be on port 8080, and the CJE masters will be on 8081 and 8082.

To start the configuration, you just need to use docker compose:

`docker-compose -f <config-file up>`
