# US Consolidated Options - Volume, OI, Greeks Schemas

Daily data providing Option Greek calculations and Open Interest and Closing Trade




## US_OPTIONS_EOD

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



### US_OPTIONS_EOD - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### US_OPTIONS_EOD - DAY Table Schema

| Field            | Data Type   | Description                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASK_CLOSE        | double      | Closing ask price                                                                                                                                                                                                                      |
| BID_CLOSE        | double      | Closing bid price                                                                                                                                                                                                                      |
| DELTA            | double      | Option delta, i.e. the rate of change of an option’s price relative to its underlying                                                                                                                                                  |
| GAMMA            | double      | Option gamma, i.e. the rate of change of an option’s delta relative to the underlying asset price                                                                                                                                      |
