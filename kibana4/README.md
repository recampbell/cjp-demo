Kibana 4 Demo
---

This project makes it easy to test Kibana4 with CJOC. If you run `docker-compose up` you will get the following services running:

* CJOC on http://${docker-machine-ip}:8080
* CJE #1 on http://${docker-machine-ip}:8081
* CJE #2 on http://${docker-machine-ip}:8082
* Elasticsearch on http://${docker-machine-ip}:9200
* Kibana 4 on http://${docker-machine-ip}:5601

Kibana 4 is already configured to talk to the Elasticsearch. You must take these additional steps after running docker-compose up:

# Configure Elasticseasrch on CJOC to use External Elasticsearches located at `http://${docker machine ip}:5601`
# Add the two client masters to CJOC
# At this point, you should start seeing metrics on the 'Performance' tab in CJOC.
