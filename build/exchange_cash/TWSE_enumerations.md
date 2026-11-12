# Taiwan Stock Exchange Enumerations

Trades, quotes, bars and book depth from the Taiwan Stock Exchange (TWSE), Taiwan’s main board, with history from September 2014. It is home to major semiconductor companies such as TSMC. Covered stocks include constituents of the TAIEX and FTSE TWSE Taiwan 50; index values are in TWSE_IDX.  A consolidated tape for both Taiwanese equity markets is provided in the TW_COMP dataset.

The following fields have Enumerations:

* ASK_COND - Quote condition applicable to the best ask
* AUCTION_TYPE - Type of auction from which an indicative auction price / auction imbalance originates.
* BID_COND - Quote condition applicable to the best bid
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

#### ASK_COND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | No condition              |
| 1                | Ask price on lower limit  |
| 2                | Ask price on upper limit  |

#### AUCTION_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                 |
|------------------|-----------------------------------------|
| A                | Unspecified auction                     |
| C                | Closing auction                         |
| I                | Intraday auction                        |
| O                | Opening auction                         |
| P                | IPO / Public offering auction           |
| S                | Settlement (EDSP) auction               |
| U                | Unscheduled auction                     |
| c                | Post-close auction                      |
| o                | Opening auction (extended hours)        |
| p                | Auction initiated by market participant |
| u                | Unscheduled auction (extended hours)    |

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

|   Enumeration ID | Enumeration Description                      |
|------------------|----------------------------------------------|
|                0 | Intraday auction uncrossing                  |
|              128 | Auction call                                 |
|               16 | Continuous trading                           |
|              160 | Closing auction call with delayed uncrossing |
|              192 | Opening auction call with delayed uncrossing |
|                4 | Closing auction uncrossing                   |
|                8 | Opening auction uncrossing                   |

#### OMD_STATUS - Enumeration

| Enumeration ID   | Enumeration Description       |
|------------------|-------------------------------|
| A                | Auction                       |
| B                | Break / Pause                 |
| C                | Closing auction               |
| D                | Delisted / Pending deletion   |
| H                | Halted                        |
| I                | Scheduled intraday auction    |
| M                | Mandatory quoting period      |
| N                | New instrument / Pre-listing  |
| O                | Opening auction               |
| P                | Pre-market                    |
| Q                | Indicative quoting period     |
| R                | Off-book trade reporting      |
| S                | Suspended                     |
| T                | Continuous trading            |
| U                | Unscheduled auction           |
| c                | Closed                        |
| i                | IPO / Public offering auction |
| n                | No market phase / Unspecified |
| o                | Order management              |
| p                | Post-market                   |
| t                | Trading at last price         |

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

