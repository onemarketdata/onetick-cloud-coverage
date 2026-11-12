# Kuwait Stock Exchange (Boursa Kuwait) Enumerations

Trades, quotes and bars from Boursa Kuwait, with history from November 2020, covering Kuwaiti equities, bonds, funds and Islamic instruments on its Premier, Main and Auction markets. Index data includes the Premier Market, Main Market and All-Share Market indices.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                5 | Buy-in                    |

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description          |
|------------------|----------------------------------|
|                1 | Enquiry (Pre-Market)             |
|                2 | Opening Auction (Pre-Open)       |
|                4 | Trading Halt                     |
|                5 | Circuit Breaker                  |
|               12 | Continuous Trading               |
|               18 | Closing Auction                  |
|               20 | Trade at Last                    |
|               21 | Close of Trading                 |
|               25 | End of Day (System Finalisation) |
|               99 | Close of Day / Market Offline    |

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

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Regular trade             |

