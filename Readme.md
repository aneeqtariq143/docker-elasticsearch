# ElasticSearch

  

## Listing of all available docker images

[Reference](https://www.docker.elastic.co/r/elasticsearch)

  

## Installation of docker 7.17

[Reference](https://www.elastic.co/guide/en/elasticsearch/reference/7.17/docker.html)

  
  

## Encrypting communications in an Elasticsearch Docker Container

[Reference](https://www.elastic.co/guide/en/elasticsearch/reference/7.17/configuring-tls-docker.html)

  

## Complete Setup
[Reference](https://www.elastic.co/guide/en/elasticsearch/reference/7.17/configuring-tls-docker.html)
  

#### Change the dns with the live domain (if you're planning to access Kibana live) 

Change the dns with the live domain in `configuration/instances.yml` at line number 26

#### Generating Certificate (one time only)

    docker compose -f ./configurations/create-certs.yml --env-file ./.env run --rm create_certs

#### Run Image
    docker compose --env-file ./.env up -d

#### Web Access URL
    https://localhost:9200/
    https://localhost:5601/