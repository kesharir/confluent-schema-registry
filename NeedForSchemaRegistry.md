## The need for a schema registry: 

- Kafka takes bytes as an input and publishes them. 
- No data verification. 

Producer -> Kafka --> Application1
              |-----> Application2 


- We need data to be self describable. 
- We need to be able to evolve data without breaking 
 downstreaming consumers. 
- We need schemas... and a schema registry. 

### What if the Kafka Brokers were verifying the messages they receive? 

- It would break what makes Kafka so good: 
  - Kafka doesn't parse or even read your data (no CPU usage)
  - Kafka takes bytes as an input without even loading them into memory 
  (that's called zero copy)
  - Kafka distributes bytes
  - As far as Kafka is concerned, it doesn't even know if your data is an integer, a 
   string etc. 

### Important point related to schema registry: 

- The Schema Registry has to be a separate component. 
- Producers and Consumers need to able to talk to schema registry.
- The schema registry must be able to reject bad data. 
- A common data format must be agreed upon:
  - It needs to support schemas.
  - It needs to support evolution
  - It needs to be lightweight
- Confluent Schema Registry solves all the above problems
- And Apache Avro as the data format. 






