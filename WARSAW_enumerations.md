# Warsaw Stock Exchange Enumerations

The Warsaw Stock Exchange (GPW) is the largest stock exchange in Central and Eastern Europe located in Poland.

The following fields have Enumerations:


* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.


* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.


* EVENT_CODE - Event that triggered an instrument status update


* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue


* MMT_ALGO_IND - Identifies whether a trade involved an algorithmic order.


* MMT_BENCHMARK_IND - Identifies whether a trade was priced according to a defined benchmark (e.g. VWAP) or reference price (e.g. midpoint of the primary market BBO), or whether it was part of a trade in multiple instruments (contingent trade or portfolio trade).


* MMT_CROSS_IND - Identifies agency cross trades, where a broker crossed two client orders outside the order book.


* MMT_DEFERRAL_TYPE - Type of publication deferral or subsequent enrichment applied to a trade report.


* MMT_DIVIDEND_IND - Identifies whether a trade includes special dividend arrangements, e.g. a trade sold cum-dividend during an ex-dividend period.


* MMT_DUP_IND - Identifies trades reported to more than one Approved Publication Arrangement.


* MMT_MKT_MECH - Market mechanism through which a trade was executed.


* MMT_MOD_IND - Identifies trade cancellations, or amendments of a previous trade.


* MMT_NEGOTIATED_IND - Indicates privately negotiated trades, or Systematic Internaliser trades exempt from pre-trade transparency.


* MMT_OFF_BOOK_AUTO_IND - Identifies whether an off-book trade report was executed via a manual or automated process.


* MMT_PRICE_FORMING_IND - Identifies whether a trade is price-forming, or contributes to the price discovery process.


* MMT_PUB_MODE - Identifies whether a trade was subject to delayed publication, and the reason for the deferral.


* MMT_TRANS_CAT - Identifies various special categories of trade.


* MMT_TRD_MODE - Trading period during which an on-book trade was executed, or origin of an off-book trade report (on-exchange / off-exchange / SI).


* ORDER_ENTRY_STATUS - Indicates the availability of order entry / modification / cancellation


* ORDER_TYPE - Type of order.


* REASON_CODE - Reason for an instrument status update


* TRADE_PERIOD - Market period during which a trade was executed.


* TRADE_TYPE - Type of trade


* UPDATE_TYPE - Type of update

# AGGRESSOR_SIDE - Enumeration

| Enumeration ID

 | Enumeration Description

 |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | ---------- | -------- |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| ‘””’

                              | Undefined (e.g. auction trades, off-book trades)

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
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| 0

                                 | Lit order book

                                                                                                                             |
| 1

                                 | Off-book

                                                                                                                                   |
| ‘””’

                              | Not applicable

                                                                                                                             |
# EVENT_CODE - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| ‘””’

                              | Unspecified

                                                                                                                                |
| A

                                 | Ask-only period

                                                                                                                            |
| B

                                 | Bid-only period

                                                                                                                            |
| C

                                 | Uncrossing

                                                                                                                                 |
| D

                                 | Scheduled re-opening cancelled

                                                                                                             |
| M

                                 | Halted

                                                                                                                                     |
| N

                                 | Initialisation

                                                                                                                             |
| O

                                 | Instrument opened

                                                                                                                          |
| P

                                 | Re-opening auction

                                                                                                                         |
| R

                                 | Halted at uncrossing

                                                                                                                       |
| Y

                                 | Start of single-sided quoting period

                                                                                                       |
| Z

                                 | End of sigle-sided quoting period

                                                                                                          |
# MKT_PHASE - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| A

                                 | Auction

                                                                                                                                    |
| CLAU

                              | Closing auction uncrossing

                                                                                                                 |
| CLCA

                              | Closing auction call

                                                                                                                       |
| CLSD

                              | Closed

                                                                                                                                     |
| COAU

                              | Core auction uncrossing

                                                                                                                    |
| COCA

                              | Core auction call

                                                                                                                          |
| COCO

                              | Core continuous

                                                                                                                            |
| COMO

                              | Core monitoring

                                                                                                                            |
| CTAL

                              | Core trading at last

                                                                                                                       |
| EAMO

                              | Early monitoring

                                                                                                                           |
| H

                                 | Halted

                                                                                                                                     |
| HALT

                              | Halted

                                                                                                                                     |
| LAMO

                              | Late monitoring

                                                                                                                            |
| LTAL

                              | Late trading at last

                                                                                                                       |
# MMT_ALGO_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not an algorithmic trade

                                                                                                                   |
| H

                                 | Algorithmic trade

                                                                                                                          |
# MMT_BENCHMARK_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not a benchmark trade

                                                                                                                      |
| B

                                 | Benchmark trade

                                                                                                                            |
| S

                                 | Reference price trade

                                                                                                                      |
# MMT_CROSS_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not a cross trade

                                                                                                                          |
| X

                                 | Agency cross trade

                                                                                                                         |
# MMT_DEFERRAL_TYPE - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | No deferral / unspecified

                                                                                                                  |
# MMT_DIVIDEND_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not applicable

                                                                                                                             |
| E

                                 | Ex-/cum-dividend

                                                                                                                           |
# MMT_DUP_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Unique trade report

                                                                                                                        |
# MMT_MKT_MECH - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not applicable

                                                                                                                             |
| 1

                                 | Central Limit Order Book

                                                                                                                   |
| 4

                                 | Off Book

                                                                                                                                   |
# MMT_MOD_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | New trade

                                                                                                                                  |
| A

                                 | Amended trade

                                                                                                                              |
| C

                                 | Trade cancellation

                                                                                                                         |
# MMT_NEGOTIATED_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not applicable

                                                                                                                             |
| 1

                                 | Negotiated trade in liquid instruments

                                                                                                     |
| 2

                                 | Negotiated trade in illiquid instruments

                                                                                                   |
| 3

                                 | Negotiated trade subject to conditions other than the market price

                                                                         |
| 4

                                 | Pre-trade transparency waiver for illiquid instrument on an SI

                                                                             |
| 5

                                 | Pre-trade transparency waiver for trade larger than Standard Market Size on an SI

                                                          |
| 6

                                 | Pre-trade transparency waivers for trade larger than Standard Market Size on an SI and illiquid instrument on an SI

                        |
| N

                                 | Negotiated trade

                                                                                                                           |
# MMT_OFF_BOOK_AUTO_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Unspecified / Not applicable

                                                                                                               |
# MMT_PRICE_FORMING_IND - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| J

                                 | Trade not contributing to the price discovery process

                                                                                      |
| N

                                 | Price not available but pending

                                                                                                            |
| P

                                 | Plain vanilla (price-forming) trade

                                                                                                        |
| T

                                 | Non-price forming (technical) trade

                                                                                                        |
# MMT_PUB_MODE - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Immediate publication

                                                                                                                      |
# MMT_TRANS_CAT - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not applicable

                                                                                                                             |
| D

                                 | Dark trade

                                                                                                                                 |
| Y

                                 | Exchange for physical

                                                                                                                      |
| Z

                                 | Package trade

                                                                                                                              |
# MMT_TRD_MODE - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| -

                                 | Not applicable

                                                                                                                             |
| 2

                                 | Continuous trading

                                                                                                                         |
| 3

                                 | At Market Close trading

                                                                                                                    |
| 5

                                 | Trade reporting (on-exchange)

                                                                                                              |
| 6

                                 | Trade reporting (off-exchange)

                                                                                                             |
| I

                                 | Intraday auction

                                                                                                                           |
| K

                                 | Closing auction

                                                                                                                            |
| O

                                 | Opening auction

                                                                                                                            |
| U

                                 | Unscheduled auction

                                                                                                                        |
# ORDER_ENTRY_STATUS - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| ‘””’

                              | Unspecified [i.e. usual order entry rules for the current market phase]

                                                                    |
| N

                                 | Order entry enabled

                                                                                                                        |
| Y

                                 | Order entry disabled

                                                                                                                       |
# ORDER_TYPE - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| L

                                 | Limit order

                                                                                                                                |
| M

                                 | Market order

                                                                                                                               |
# REASON_CODE - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| ‘””’

                              | Unspecified

                                                                                                                                |
| A

                                 | Max number of orders exceeded

                                                                                                              |
| C

                                 | Trade price outside dynamic collars

                                                                                                        |
| G

                                 | Regulatory halt

                                                                                                                            |
| M

                                 | Manual halt

                                                                                                                                |
| R

                                 | No liquidity provider quote

                                                                                                                |
| S

                                 | Trade price outside static collars

                                                                                                         |
| W

                                 | Knocked out

                                                                                                                                |
| X

                                 | Underlying halted

                                                                                                                          |
# TRADE_PERIOD - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| A

                                 | Other auction [e.g. after-hours odd lot auction]

                                                                                           |
| C

                                 | Closing auction

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
| U

                                 | Unscheduled auction

                                                                                                                        |
| -

                                 | Regular trading

                                                                                                                            |
| ‘””’

                              | Not applicable

                                                                                                                             |
# TRADE_TYPE - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| 0

                                 | Regular trade

                                                                                                                              |
| 1

                                 | Cross trade

                                                                                                                                |
| 4

                                 | Valuation trade

                                                                                                                            |
| 5

                                 | Internalised trade

                                                                                                                         |
| 6

                                 | Internalised cross trade

                                                                                                                   |
| I

                                 | Public offering

                                                                                                                            |
| O

                                 | Block trade

                                                                                                                                |
| R

                                 | Reported trade

                                                                                                                             |
| S

                                 | Buy-in / sell-out

                                                                                                                          |
| T

                                 | Tender offer

                                                                                                                               |
# UPDATE_TYPE - Enumeration

| Enumeration ID

                    | Enumeration Description

                                                                                                                    |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| A

                                 | Add

                                                                                                                                        |
| D

                                 | Delete

                                                                                                                                     |
| M

                                 | Modify

