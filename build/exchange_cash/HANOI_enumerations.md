# Hanoi Stock Exchange Enumerations

Trades, quotes and bars from the Hanoi Stock Exchange (HNX), Vietnam’s second stock exchange after the Ho Chi Minh Stock Exchange, with history from August 2011. HNX was formed in 2009 from the Hanoi Securities Trading Center and handles trading of stocks, bonds and derivatives, and also runs UPCoM, the market for unlisted public companies. Covered stocks include constituents of the HNX-Index and HNX30.

The following fields have Enumerations:

* AUCTION_TYPE - Type of auction from which an indicative auction price / auction imbalance originates.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

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

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description                |
|------------------|----------------------------------------|
|                0 | Pre-Open / Day Start                   |
|                1 | Periodic Opening Session               |
|                4 | Continuous Trading Session (Morning)   |
|               12 | Intermission (Lunch Break)             |
|               14 | Continuous Trading Session (Afternoon) |
|               16 | Periodic Closing Session (ATC)         |
|               18 | PLO After-Hours Trading Session        |
|               97 | Market Closed                          |

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

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| A                | Auction                   |
| C                | Closing auction           |
| T                | Trading at closing price  |

#### TRADE_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Regular trade             |
|                1 | Put-through trade         |
|                3 | Auction trade             |

