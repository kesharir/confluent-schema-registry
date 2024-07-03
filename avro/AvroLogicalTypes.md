## Avro Logical Types: 

- Avro has a concept of logical types used to give 
  more meaning to already existing primitive types.
- The most commonly used are: 
  - decimal (bytes)
  - date (int) - number of days since unix epoch (Jan 1st 1970)
  - time-millis (long) - number of milliseconds after midnight, 00:00:00.000
  - timestamp-millis (long) - the number of milliseconds from the unix-epoch, 
    1 January 1970 00:00:00.000 UTC

### How to use a logical type?

- To use a logical type, just add "logicalType":"time-millis" to the filed name and it 
  will help avro schema processors to inter a specific type. 

- Example: Customer Signup timestamp: 

```
{
  "name":"signup_ts",
  "type":"long",
  "logicalType":"timestamp-millis"
}
```

- Note: Logical types are new (1.7.7), not fully supported by all languages and don't play 
 nicely with unions. Be careful when using them. 

