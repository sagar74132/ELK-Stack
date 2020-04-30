# ELK-Stack
docker compose file to setup Elasticsearch, logstash and Kibana (ELK) stack.

## How to use

Clone this repo and use Docker-compose.yml file in docker-terminal to install & start the ELK-Stack or create the Docer-compose.yml file and paste the code in it given below -

```
# Author: Sagar Singh
# Docker repo: https://hub.docker.com/u/sa40039455

version: '3.3'

services:
    
    elasticsearch:
        image: elasticsearch:2
        volumes:
            - ./esdata/:/usr/share/elasticsearch/data/
        ports: 
            - 9200:9200
            - 9300:9300
    
    logstach:
        image: logstash:7.6.2
        ports:
            - 5044:5044
    
    kibana:
        image: kibana:4.6
        ports: 
            - 5601:5601
```
