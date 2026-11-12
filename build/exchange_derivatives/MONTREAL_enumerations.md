# Montreal Exchange Enumerations

Futures, options and spreads with Trades, Quotes, bars and book depth from the Montréal Exchange (MX), Canada’s derivatives exchange owned by TMX Group, with futures from December 2009 and options from May 2025. Key contracts include S&P/TSX 60 index futures (SXF), three-month CORRA futures, ten-year Government of Canada bond futures (CGB) and Canadian equity options.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* CALL_PUT_IND - “C” - Call option, “P” - Put option
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

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

| Enumeration ID   | Enumeration Description        |
|------------------|--------------------------------|
| B                | Post-trading                   |
| C                | Consultation start             |
| c                | Not trading                    |
| E                | No cancellation                |
| F                | Consultation end               |
| f                | Forbidden                      |
| I                | Prohibited                     |
| M                | Mini-batch                     |
| N                | Market Operations intervention |
| O                | Opening                        |
| P                | Pre-opening                    |
| r                | Pre-opening                    |
| S                | Continuous trading             |
| s                | Suspended                      |
| Z                | Interrupted                    |

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
| I                | Intraday auction          |
| O                | Opening auction           |
| U                | Unscheduled auction       |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| 0                | Regular trade             |
| 12               | Delta trade               |
| 13               | Committed block           |
| 14               | Late trade                |
| 16               | Strategy leg trade        |
| 2                | Block trade               |
| 22               | Exchange for Risk         |
| 24               | Committed trade           |
| 25               | Basis on Close            |
| 26               | Price/volume adjustment   |
| 4                | Cross trade               |
| 5                | Exchange for Physical     |
| 56               | Trade correction          |
| 9                | Implied trade             |
| A                | As-of trade               |
| C                | Contingent trade          |
| F                | Riskless basis cross      |

