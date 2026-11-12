# Nextrade ATS Enumerations

Trades, Quotes and Book depth from Nextrade (NXT), South Korea’s first licensed alternative trading system, which launched in March 2025 to compete with the Korea Exchange, with history from September 2026. NXT offers pre-market and after-market sessions outside regular Korea Exchange hours and trades KOSPI- and KOSDAQ-listed stocks.  A consolidated tape for both Korean equity markets is provided in the KR_COMP dataset.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* AUCTION_TYPE - Type of auction from which an indicative auction price / auction imbalance originates.
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* TRADE_TYPE - Type of trade
* TRADE_PERIOD - Market period during which a trade was executed.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description                          |
|------------------|--------------------------------------------------|
| ‘””’             | Undefined (e.g. auction trades, off-book trades) |
| B                | Buy                                              |
| S                | Sell                                             |

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

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Regular trade             |
| BLK              | Block trade               |
| BKT              | Basket trade              |
| CL               | Trade at closing price    |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description              |
|------------------|--------------------------------------|
| E                | Extended hours (early session)       |
| L                | Extended hours (late session)        |
| T                | Trading at last price                |
| U                | Unscheduled auction                  |
| o                | Opening auction (extended hours)     |
| u                | Unscheduled auction (extended hours) |
| -                | Regular trading                      |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |

