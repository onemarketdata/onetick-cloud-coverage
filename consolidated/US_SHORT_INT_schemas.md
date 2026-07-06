# FINRA - US Equities Short Interest / Short Volume Schemas

FINRA US Equity short interest summary every two weeks, plus trade reports, and daily short volume through Trade Reporting Facilities.  FINRA Daily Short Sale Volume is stored in the DAY table.  This is populated daily.  Monthly Short Sale Volume is stored in the TRD and SHORT_INT tables, and is populated monthly, approximately 8 days after the month is complete.  The TRD table reports data per day, while the SHORT_INT table reports data twice per month.

## US_SHORT_INT

Database includes the following tick types:


* DAY - Daily price and statistical data, e.g. closing price, settlement price, open interest


* SHORT_INT - Short Interest Statistics every 2 weeks


* TRD - Trades

### US_SHORT_INT - DAY

Daily price and statistical data, e.g. closing price, settlement price, open interest

### US_SHORT_INT - DAY Table Schema

| Field

 | Data Type

 | Description

 |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| OMDSEQ

                      | uint

                                                                                                                | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
| SHORT_EXEMPT_VOLUME

         | double

                                                                                                              | Total short selling volume exempt from Regulation SHO restrictions

                                                                                                                                                                                |
| SHORT_VOLUME

                | double

                                                                                                              | Total short selling volume on the current trading day

                                                                                                                                                                                             |
| TRF

                         | string[4]

                                                                                                           | Trade Reporting Facility used to report a trade (for trades reported to FINRA)

                                                                                                                                                                    |
| VOLUME

                      | double

                                                                                                              | DAY: Total volume traded on the current trading day  TRD_1M, VWAP_1H: Total volume of eligible trades in the current bar interval

                                                                                                                 |
### US_SHORT_INT - SHORT_INT

Short Interest Statistics every 2 weeks

### US_SHORT_INT - SHORT_INT Table Schema

| Field

                       | Data Type

                                                                                                           | Description

                                                                                                                                                                                                                                       |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| AVG_DAILY_VOLUME

            | double

                                                                                                              | Average daily traded volume

                                                                                                                                                                                                                       |
| OMDSEQ

                      | uint

                                                                                                                | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
| PREV_SHORT_INT

              | double

                                                                                                              | Previous short interest

                                                                                                                                                                                                                           |
| SHORT_INT

                   | double

                                                                                                              | Total short position held in the security

                                                                                                                                                                                                         |
| SHORT_INT_CHG

               | double

                                                                                                              | Short interest net change

                                                                                                                                                                                                                         |
| SHORT_INT_CHG_PCT

           | double

                                                                                                              | Short interest percentage change

                                                                                                                                                                                                                  |
| SHORT_INT_DAYS_TO_COVER

     | double

                                                                                                              | Short interest as a multiple of the average daily volume

                                                                                                                                                                                          |
### US_SHORT_INT - TRD

Trades

### US_SHORT_INT - TRD Table Schema

| Field

                       | Data Type

                                                                                                           | Description

                                                                                                                                                                                                                                       |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| OMDSEQ

                      | uint

                                                                                                                | Sequence number allowing ticks of different types at the same timestamp to be sorted into the correct chronological order.  e.g. if a trade and a quote have the same timestamp, the one with the lower value of OMDSEQ arrived first.

            |
| PRICE

                       | double

                                                                                                              | TRD: Trade price, IDX: Index value, IND: Indicative price, PRL: Price point to which the depth entry relates, PRL_FULL: Order price, FIXING: Fixing price, RFC: Price associated with a Request for Cross

                                         |
| SHORT_TYPE

                  | string[1]

                                                                                                           | Type of short sale

                                                                                                                                                                                                                                |
| SIZE

                        | int

                                                                                                                 | TRD: Trade size, IND: Indicative size, PRL: Size at the relevant price point, PRL_FULL: Order size, RFQ: Size associated with a Request for Quote, RFC: Size associated with a Request for Cross

                                                  |
| TRF

                         | string[1]

                                                                                                           | Trade Reporting Facility used to report a trade (for trades reported to FINRA)

