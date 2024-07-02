## Avro Complex Types: 

- In Avro you have complex types such as : 
  - Enums
  - Arrays
  - Maps
  - Unions
  - Calling other schemas as types
- Lets go over these types one by one


### Enums: 
Example: 
CustomerStatus
- Bronze 
- Silver 
- Gold

```
{
    "type":"enum",
    "name":"CustomerStatus",
    "symbols":["BRONZE", "SILVER", "GOLD"]
}    
```

- Note once an enum is set, changing the enum values is forbidden if you want to maintain
compatibility

### Arrays: 

```
{
    "type":"array",
    "items":"string"
}
```


### Maps : Keys and Values


```
{
    "type":"map",
    "values":"string"
}
```

### Unions: 

- Unions can allow a field value to take different types. 
- Example: ["string", "int", "boolean"]
- If defaults are defined, the default must be of the type of the first item in the union.
  (So, in this case, "string").

```
{
    "name": "middle_name",
    "type": ["null", "string"],
    "default": null
}
```

