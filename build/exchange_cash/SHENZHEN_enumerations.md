# Shenzhen Stock Exchange Enumerations

Trades, quotes and bars from the Shenzhen Stock Exchange (SZSE), one of mainland China’s two stock exchanges, with history from June 2015, covering the main board and ChiNext growth market, A-shares and B-shares, and Shenzhen-Hong Kong Stock Connect. Covered stocks include constituents of the SZSE Component Index, ChiNext Index and CSI 300.

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
|                1 | Off-book                  |

#### MKT_PHASE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| 65               | After-hours trading       |
| 66               | Break                     |
| 67               | Closing auction           |
| 69               | Closed                    |
| 72               | Temporary suspension      |
| 79               | Opening auction           |
| 83               | Start of day              |
| 84               | Continuous trading        |
| 86               | Volatility halt           |
| SUSP             | Suspended                 |

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

| Enumeration ID   | Enumeration Description       |
|------------------|-------------------------------|
| ‘””’             | Regular trade                 |
| 0                | Regular trade                 |
| 1                | After-hours fixed price trade |
| 102              | Negotiated trade              |
| 103              | Click trade                   |
| 104              | Inquiry trade                 |
| 105              | Bidding trade                 |

