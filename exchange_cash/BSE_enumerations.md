# BSE (Bombay Stock Exchange) Enumerations

The Bombay Stock Exchange is one of the largest securities markets. It is located on Dalal Street, Mumbai and lists over 6000 companies.

The following fields have Enumerations:


* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.


* CALL_PUT_IND - “C” - Call option, “P” - Put option


* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue


* TRADE_PERIOD - Market period during which a trade was executed.


* TRADE_TYPE - Type of trade

# BOOK_TYPE - Enumeration

| Enumeration ID

 | Enumeration Description

 |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 0

                           | Lit order book

                                                                                                      |
| 1

                           | Off-book

                                                                                                            |
| 3

                           | Odd lot book

                                                                                                        |
# CALL_PUT_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| C

                           | Call option

                                                                                                         |
| P

                           | Put option

                                                                                                          |
# MKT_PHASE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| ‘””’

                        | No market phase

                                                                                                     |
| A

                           | Periodic call auction

                                                                                               |
| CS

                          | Closing session

                                                                                                     |
| CTN

                         | Continuous trading

                                                                                                  |
| EOD

                         | End of day session

                                                                                                  |
| MQ

                          | Member query

                                                                                                        |
| OM

                          | Order matching

                                                                                                      |
| PCS

                         | Post-close session

                                                                                                  |
| PO

                          | Pre-open

                                                                                                            |
| SOD

                         | Start of day

                                                                                                        |
| SUSP

                        | Suspended

                                                                                                           |
# TRADE_PERIOD - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | Regular trading

                                                                                                     |
| I

                           | Intraday auction

                                                                                                    |
| O

                           | Opening auction

                                                                                                     |
| T

                           | Trading at closing price

                                                                                            |
# TRADE_TYPE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| ‘””’

                        | Regular trade

                                                                                                       |
| BLK

                         | Block trade

                                                                                                         |
| BT

                          | Bunched trade [Aggregated trade where the individual executions are not sent by the exchange]

