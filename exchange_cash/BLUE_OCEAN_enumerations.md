# Blue Ocean ATS Enumerations

Blue Ocean ATS (BOATS) is a US-based Alternative Trading System (ATS) run by Blue Ocean Technologies, enabling trading of U.S. stocks (NMS) during non-traditional hours, specifically 8 PM to 4 AM ET, Sunday to Thursday, bridging the overnight gap

The following fields have Enumerations:


* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.


* TRADE_TYPE - Type of trade


* TRADE_PERIOD - Market period during which a trade was executed.


* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.


* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue


* REASON_CODE - Reason for an instrument status update


* SHORT_SALE_RESTRICTION - Indicates whether short selling is permitted


* UPDATE_TYPE - Type of update


* ORDER_TYPE - Type of order.

# AGGRESSOR_SIDE - Enumeration

| Enumeration ID

 | Enumeration Description

 |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| ‘””’

                        | Undefined (e.g. auction trades, trades against hidden liquidity)

                                                    |
| B

                           | Buy

                                                                                                                 |
| S

                           | Sell

                                                                                                                |
# TRADE_TYPE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| ‘””’

                        | Regular trade

                                                                                                       |
| H

                           | Trade against hidden liquidity

                                                                                      |
# TRADE_PERIOD - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| -

                           | Regular trading

                                                                                                     |
# BOOK_TYPE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| 0

                           | Lit order book

                                                                                                      |
# MKT_PHASE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| ‘””’

                        | No market phase

                                                                                                     |
| 1

                           | Opening (pre-market)

                                                                                                |
| 2

                           | Trading

                                                                                                             |
| 3

                           | Post-trading

                                                                                                        |
| 4

                           | Closed

                                                                                                              |
| H

                           | Halted

                                                                                                              |
| P

                           | Paused

                                                                                                              |
| Q

                           | Quoting

                                                                                                             |
# REASON_CODE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| ‘””’

                        | Unspecified

                                                                                                         |
| A

                           | Administrative

                                                                                                      |
| R

                           | Regulatory

                                                                                                          |
| X

                           | None

                                                                                                                |
# SHORT_SALE_RESTRICTION - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| 0

                           | No short sellling restriction

                                                                                       |
| 1

                           | Short selling restriction in effect

                                                                                 |
# UPDATE_TYPE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| A

                           | Add

                                                                                                                 |
| D

                           | Delete

                                                                                                              |
| F

                           | Fill

                                                                                                                |
| M

                           | Modify

                                                                                                              |
| P

                           | Partial fill

                                                                                                        |
# ORDER_TYPE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                             |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| L

                           | limit order

