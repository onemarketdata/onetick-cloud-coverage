# US Consolidated Options (OPRA) EOD - OPRA Daily Volume, OI and Greeks Sample Schemas

Daily data providing Option Greek calculations and Open Interest and Closing Trade.  Options on AAPL, NVDA, QQQ, SPY and TSLA are included in the sample covering January 2025.




## US_OPTIONS_EOD_SAMPLE

Database includes the following tick types:

* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest
* STAT - Static data, e.g. ISIN, description, security type



### US_OPTIONS_EOD_SAMPLE - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

#### US_OPTIONS_EOD_SAMPLE - DAY Table Schema

| Field            | Data Type   | Description                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ASK_CLOSE        | double      | Closing ask price                                                                                                                                                                                                                      |
| BID_CLOSE        | double      | Closing bid price                                                                                                                                                                                                                      |
| DELTA            | double      | Option delta, i.e. the rate of change of an option’s price relative to its underlying                                                                                                                                                  |
| GAMMA            | double      | Option gamma, i.e. the rate of change of an option’s delta relative to the underlying asset price                                                                                                                                      |
