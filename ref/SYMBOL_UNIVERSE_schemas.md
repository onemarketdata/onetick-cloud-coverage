# Symbol Universe for all databases Schemas

Symbol Universe for all databases. Keyed on Database and Security Type.




## SYMBOL_UNIVERSE

Database includes the following tick types:

* STAT - Static data, e.g. ISIN, description, security type



### SYMBOL_UNIVERSE - STAT

Static data, e.g. ISIN, description, security type

#### SYMBOL_UNIVERSE - STAT Table Schema

| Field             | Data Type   | Description                                                                                                                                                                                                                                |
|-------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BSYM              | string[100] | Bloomberg Symbol                                                                                                                                                                                                                           |
| CALL_PUT_IND      | string[2]   | C - Call option, P - Put option                                                                                                                                                                                                            |
