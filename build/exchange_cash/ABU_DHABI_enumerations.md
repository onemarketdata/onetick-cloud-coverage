# Abu Dhabi Securities Exchange Enumerations

Trades, quotes and bars from the Abu Dhabi Securities Exchange (ADX), with history from June 2016, covering equities, bonds, ETFs and futures of UAE companies. Index data is included, such as the FTSE ADX General Index (FADGI), the main benchmark for Abu Dhabi-listed stocks.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |

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
| C                | Closing auction           |
| O                | Opening auction           |
| T                | Trading at closing price  |
| U                | Unscheduled auction       |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Regular trade             |
| 1                | Regular trade             |
| 2                | Block trade               |
| 3                | Auction trade             |

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                8 | Pre-Close                 |
|               14 | Trade-At-Last / TAL       |
|               12 | Closed                    |
|                5 | Open / Ongoing Trading    |

