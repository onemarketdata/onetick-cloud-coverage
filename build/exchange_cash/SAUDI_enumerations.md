# Saudi Stock Exchange Enumerations

Trades, quotes and bars from the Saudi Exchange (Tadawul), the largest stock exchange in the Middle East, with history from June 2014. It covers the Main Market and the Nomu parallel market, ETFs, REITs and sukuk. Covered stocks include constituents of the Tadawul All Share Index (TASI), such as Saudi Aramco.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

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

#### TRADE_TYPE - Enumeration

|   Enumeration ID | Enumeration Description                |
|------------------|----------------------------------------|
|               10 | Negotiated cross trade                 |
|               15 | Automatch trade [until 20150910]       |
|               19 | Small automatch trade [until 20150910] |
|               26 | Put-through trade [until 20150910]     |
|                3 | Automatch trade                        |
|                4 | Small automatch trade                  |
|                5 | Put-through trade                      |
|                6 | Put-through cross trade                |
|                7 | Small put-through trade                |
|                8 | Small put-through cross trade          |
|                9 | Negotiated trade                       |

