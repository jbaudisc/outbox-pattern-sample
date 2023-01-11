# Getting Started

An example for change data capture with Kafka as described in https://medium.com/@hpgrahsl/communicating-data-changes-across-service-boundaries-safely-129c4eb5db8
Adapted from https://github.com/hpgrahsl/outbox-pattern-sample with additional
docker-compose setup, Debezium Config and updated dependencies.



### How to run
Start the Lenses.io's streaming platform including kafka, zookeeper,
Kafka Connect, Schema Registry with the UI and MySql using docker-compose:

```
cd etc
docker-compose up
```

Lenses.io UI can be accessed at http://localhost:3030

Navigate to the [Kafka Connect UI](http://localhost:3030/kafka-connect-ui/#/cluster/fast-data-dev) and
add the Debezium connector by pasting the JSON from [/etc/dbz-mysql-outbox-connector.json](/etc/dbz-mysql-outbox-connector.json)

Now start the `OutboxPatternApplication` and view the events in topic
[outbox-demo.outbox_event](http://localhost:3030/kafka-topics-ui/#/cluster/fast-data-dev/topic/n/dbserver1.outbox-demo.outbox_event/)




