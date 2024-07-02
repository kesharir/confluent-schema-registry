## Introduction to Avro: 

### An Evolution of data Comma Separated Values (CSV): 

- First CSV: 

rownum | column1 |column2 |column3 | 
-------|-------|-------|-------
row1|a|b|c
row2|a|b|c

### Advantages: 

    - Easy to parse 
    - Easy to read 
    - Easy to make sense of 

### DisAdvantages: 

    - The data types of elements has to be inferred and is not a guarantee
    - Parsing becomes tricky when data contains commas
    - Column names may or may not be there 

- Relational Table Definition: 
  ```
  Relation table definitions add types:
  ```   
### Advantages:   
```
  - Data is fully typed.
  - Data fits in a table. 
```

### Disadvantages: 
```
  - Data has to be flat
  - Data is stored in a database and data definition will be different for each database. 
```

- JSON: 

### Advantages: 
```
  - Data can take any form (arrays, nested elements)
  - JSON is a widely accepted format on the web
  - JSON can be easily shared over a network
```

### Disadvantages: 
```
- Data has no schema enforcing. 
- JSON Objects can be quite big in size because of repeated keys. 
```

- AVRO:

```
  - AVRO is defined by a schema (schema is written in JSON)
  - To get started, you can view Avro as JSON with a schema attached to it. 
```

### Advantages: 
```
  - Data is fully typed. 
  - Data is compressed automatically (less CPU usage)
  - Schema (defined using JSON) comes along with the data
  - Documentation is embedded in the schema
  - Data can be read across any language
  - Schema can evolve over time, in a safe manner (schema evolution)
```

### Disadvantages: 

```
  - Avro support for some languages may be lacking (but the main ones is fine). 
  - Can't "print" the data without using avro tools (because its compressed and serialised)
```



## Avro vs Protobufvs Thrift vs Parquet vs ORC .... :

```
- Overall, all of these data formats achieve pretty much the same goal.
- At kafka's level, what we care about is one message being explicit and fully described 
  as we are dealing with streaming (so no ORC Parquet etc). 
- Avro has good support from Hadoop based technologies like Hive.
- Avro has been chosen as the only supported data format from Confluent Schema Registry
  so will just go along with that!
```