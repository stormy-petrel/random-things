# Confluent Platform QuickStart

- [Download and start Confluent Platform](https://docs.confluent.io/platform/current/platform-quickstart.html#step-2-create-ak-topics-for-storing-your-data)
- [ksqlDB QuickStart](https://ksqldb.io/quickstart.html)
- [Rest-Proxy](https://docs.confluent.io/platform/current/kafka-rest/index.html#features)


# Kafka Topic Management

- [Modify partition count](https://support.confluent.io/hc/en-us/articles/360040094151-How-to-increase-the-partition-count-for-a-Confluent-Cloud-hosted-topic) 
   - !!! BE CAREFUL.. This doesn't not work for topics storing aggregated results calculated by ksqlDB because the state store is managed by ksqlDB.
       - And if there are joins using the topic as source, it can be complicated.  So potentially, the topic needs to be copied.  
   - Need the tar version of the [Confluent Platform](https://docs.confluent.io/platform/current/platform-quickstart.html#step-1-download-and-start-cp)
   - The configuration file required can be generated on ConfluentCloud UI:  Clients-> `New Client` button brining up pop-up windoer with auto-filled info  

# Kafka Persistent Query
- [Monitoring Persistent Query](https://docs.confluent.io/cloud/current/ksqldb/monitoring-ksqldb.html#monitoring-persistent-queries)

# ksqlDB issues
- [pull query deadlock](https://github.com/confluentinc/ksql/issues/8816)


# Install Confluent HTTP Sink Connector
- [HTTP Sink] https://www.confluent.io/hub/confluentinc/kafka-connect-http
