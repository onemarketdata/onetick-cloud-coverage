# ICE Europe Commodities Enumerations

ICE Europe Commodities provides trading in commodity futures and options like crude oil, natural gas, power, emissions, and more.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* CALL_PUT_IND - “C” - Call option, “P” - Put option
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* ORDER_TYPE - Type of order.
* TRADE_TYPE - Type of trade

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description                                          |
|------------------|------------------------------------------------------------------|
| ‘””’             | Undefined (e.g. auction trades, implied trades, off-book trades) |
| B                | Buy                                                              |
| S                | Sell                                                             |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |

#### CALL_PUT_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Call option               |
| P                | Put option                |

#### MKT_PHASE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| 1                | Pre-open                  |
| 2                | Pre-close                 |
| C                | Closed                    |
| E                | Expired                   |
| O                | Open                      |

#### ORDER_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| I                | Implied order             |
| L                | Limit order               |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                                  |
|------------------|----------------------------------------------------------|
| 0                | Standard trade                                           |
| AA               | Asset Allocation                                         |
| AAL              | Asset allocation leg trade (System priced)               |
| ADJ              | Adjusted trade                                           |
| BAS              | Basis trade                                              |
| BLK              | Block trade                                              |
