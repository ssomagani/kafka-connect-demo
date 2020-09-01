# kafka-connect-demo

## Running Instructions:

docker-compose -f docker-compose-single.yml up

### Standalone
 connect-standalone config/connect-standalone-sink.properties config/file-sink-standalone.properties
 
 connect-standalone config/connect-standalone-source.properties config/file-source-standalone.properties 

### Distributed
connect-distributed config/connect-distributed-source.properties config/file-source-distributed.properties

connect-distributed config/connect-distributed-sink.properties config/file-sink-distributed.properties

## Monitoring commands:
/opt/kafka/bin/kafka-topics.sh --bootstrap-server=kafka-1:9092,kafka-2:9092,kafka-3:9092 --list

/opt/kafka/bin/kafka-console-consumer.sh --bootstrap-server=localhost:9092 --topic=standalone_topic --from-beginning
