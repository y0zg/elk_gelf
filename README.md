Run `docker-compose -f docker-compose-orig.yml up`
Login to kibana `http://localhost:5601/app/kibana`
In management tab create index `logstash-*.` \

containers in docker-compose yml should contain gelf driver.
```
        logging:
          driver: gelf
          options:
            gelf-address: udp://localhost:12201
            tag: "staging"
```         
Note: in Elasticsearch term index is equal to database
