- Floats and Doubles are floating binary point types. 
- Decimal is a floating decimal point type. 
  - Some decimals cannot be represent accurately as floats or doubles!
- People use floats and doubles for scientific computations (imprecise computations) because 
    these type are fast
- People use decimals for money. That's why it got created in the first place. Use decimal 
    when you need "exactly accurate results".
- Avro introduces a decimal logical type, but its underlying type is "bytes". That means that if 
    you print an avro as json, you won't see the decimal value, just some gibberish. 
- Additionally, transforming these bytes into a decimal is very error prone if the language
    library you are using did not implement that feature. The official Avro library for java did
    not get it right the first time! (AVRO-1869)
- Instructor advises against using decimals. 
- It the meantime here are the alternatives" 
  - use "string" to represent decimal value
  - create your own decimal type: 
    - integer part
    - decimal part

