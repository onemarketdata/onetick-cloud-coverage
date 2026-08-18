# Taipei Exchange Enumerations

The Taipei Exchange is a stock exchange in Taiwan that trades Taiwanese equities and bonds.

The following fields have Enumerations:

* ASK_COND - Quote condition applicable to the best ask
* BID_COND - Quote condition applicable to the best bid
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

#### ASK_COND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | No condition              |
| 1                | Ask price on lower limit  |
| 2                | Ask price on upper limit  |

#### BID_COND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | No condition              |
| 1                | Bid price on lower limit  |
| 2                | Bid price on upper limit  |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |
|                3 | Odd lot book              |
|                6 | Auction book              |

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description                                   |
|------------------|-----------------------------------------------------------|
|                0 | Auction uncrossing (Main Board) / Closed (Emerging Board) |
|                1 | Continuous trading                                        |
|               10 | Closing auction call with delayed uncrossing              |
|               12 | Opening auction call with delayed uncrossing              |
|                2 | Start of day                                              |
|                8 | Auction call                                              |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description                          |
|------------------|--------------------------------------------------|
| -                | Regular trading                                  |
| A                | Other auction [e.g. after-hours odd lot auction] |
| C                | Closing auction                                  |
| I                | Intraday auction                                 |
| O                | Opening auction                                  |
| T                | Trading at closing price                         |
| U                | Unscheduled auction                              |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Regular trade             |
| F                | Fixed price auction trade |
| O                | Odd lot trade             |

