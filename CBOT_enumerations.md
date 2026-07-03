# CBOT Futures Enumerations

The CME Chicago Board of Trade (CBOT) offers trading in futures on agricultural commodities, interest rates, and equity indices.

The following fields have Enumerations:


* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.


* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.


* CALL_PUT_IND - “C” - Call option, “P” - Put option


* EVENT_CODE - Event that triggered an instrument status update


* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue


* ORDER_TYPE - Type of order.


* REASON_CODE - Reason for an instrument status update


* TRADE_PERIOD - Market period during which a trade was executed.


* TRADE_TYPE - Type of trade


* UPDATE_TYPE - Type of update

# AGGRESSOR_SIDE - Enumeration

| Enumeration ID

 | Enumeration Description

 |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| ‘””’

                        | Undefined (e.g. auction trades, implied trades, off-book trades)

                                                       |
| B

                           | Buy

                                                                                                                    |
| S

                           | Sell

                                                                                                                   |
# BOOK_TYPE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| 0

                           | Lit order book

                                                                                                         |
| 1

                           | Off-book

                                                                                                               |
# CALL_PUT_IND - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| C

                           | Call option

                                                                                                            |
| P

                           | Put option

                                                                                                             |
# EVENT_CODE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| 0

                           | No special event

                                                                                                       |
| 1

                           | No cancel

                                                                                                              |
| 4

                           | New trading day

                                                                                                        |
| 5

                           | Implied matching on

                                                                                                    |
| 6

                           | Implied matching off

                                                                                                   |
# MKT_PHASE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| 15

                          | New price indication

                                                                                                   |
| 17

                          | Trading

                                                                                                                |
| 18

                          | Not available for trading

                                                                                              |
| 2

                           | Halted

                                                                                                                 |
| 20

                          | Unspecified

                                                                                                            |
| 21

                          | Pre-open

                                                                                                               |
| 24

                          | Pre-cross

                                                                                                              |
| 25

                          | Cross

                                                                                                                  |
| 26

                          | Post-close

                                                                                                             |
| 4

                           | Closed

                                                                                                                 |
# ORDER_TYPE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| I

                           | Implied order

                                                                                                          |
| L

                           | Limit order

                                                                                                            |
# REASON_CODE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| 0

                           | Scheduled transition

                                                                                                   |
| 1

                           | Surveillance intervention

                                                                                              |
| 2

                           | Market event

                                                                                                           |
| 3

                           | Instrument activation

                                                                                                  |
| 4

                           | Instrument expiration

                                                                                                  |
| 5

                           | Unspecified

                                                                                                            |
| 6

                           | Recovery

                                                                                                               |
# TRADE_PERIOD - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| -

                           | Regular trading

                                                                                                        |
| A

                           | Auction

                                                                                                                |
# TRADE_TYPE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| -

                           | Regular trade

                                                                                                          |
| BLK

                         | Block trade [Note: price may be null for block trades in spreads - this is because CME does not always publish a price]

 |
| BLKL

                        | Leg of a strategy block trade

                                                                                           |
| IMP

                         | Implied trade [Trade where either the buy or the sell side was an implied price]

                                        |
| LEG

                         | Strategy leg trade [Synthetic trade reported on each outright leg when two spread orders are matched - price is always null]

 |
| RFC

                         | Request for Cross (RFC) trade

                                                                                                |
# UPDATE_TYPE - Enumeration

| Enumeration ID

              | Enumeration Description

                                                                                                      |
| --------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
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
| R

                           | Refresh

