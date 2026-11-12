# B3 (Bovespa) - Equities + Equity Options Enumerations

Trades, quotes and bars for B3’s equities segment (formerly Bovespa), Brazil’s stock exchange, covering stocks, ETFs, BDRs and equity options, with equities from May 2008 and indices from January 2014. Index data includes the Ibovespa, Brazil’s main equity benchmark, and other B3 indices.

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

|   Enumeration ID | Enumeration Description               |
|------------------|---------------------------------------|
|               02 | Trading halt (Pause)                  |
|               04 | No-Open (Close)                       |
|               17 | Ready to trade (Open)                 |
|               18 | Not available for trading (Pre-close) |
|               21 | Pre-Open                              |
|              101 | Final Closing Call                    |

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

| Enumeration ID   | Enumeration Description      |
|------------------|------------------------------|
| -                | Regular trading              |
| C                | Closing auction              |
| L                | Outside hours (Late session) |
| O                | Opening auction              |
| U                | Unscheduled auction          |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description         |
|------------------|---------------------------------|
| 0                | Regular trade                   |
| 1                | Cross trade                     |
| 24               | After-hours trade               |
| 25               | Retail Liquidity Provider trade |
| 26               | Out of sequence trade           |
| RLP              | Retail Liquidity Provider trade |

