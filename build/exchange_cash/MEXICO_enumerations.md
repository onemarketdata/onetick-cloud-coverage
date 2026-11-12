# Mexico Stock Exchange (BMV) Enumerations

Trades, quotes and bars from the Bolsa Mexicana de Valores (BMV), Mexico’s largest stock exchange, with history from January 2014. It covers Mexican stocks, FIBRAs and the SIC (Sistema Internacional de Cotizaciones), where foreign securities trade in Mexico. Covered stocks include constituents of the S&P/BMV IPC; for trading on both BMV and BIVA, use MX_COMP.

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
|                2 | Dark book                 |
|                6 | Auction book              |

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description                                   |
|------------------|-----------------------------------------------------------|
|                0 | Order cancellation                                        |
|                1 | Opening auction                                           |
|               10 | Suspended series                                          |
|               11 | Listing suspended                                         |
|               12 | Unscheduled auction due to breach of listing requirements |
|               13 | Orderbook cleared after continuous auction                |
|               14 | Orderbook cleared after intraday auction                  |
|               15 | News pending                                              |
|               16 | Settlement auction                                        |
|               17 | Extraordinary settlement auction                          |
|               18 | Single daily auction for CKDes                            |
|               19 | Closed                                                    |
|                2 | Pre-market                                                |
|                3 | Auction allocation (uncrossing)                           |
|                4 | Auction allocation completed                              |
|                5 | End of auction                                            |
|                6 | Continuous trading                                        |
|                7 | Volatility auction                                        |
|                8 | Continuous auction due to >20 days of inactivity          |
|                9 | Demerger / spin-off auction                               |

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

| Enumeration ID   | Enumeration Description           |
|------------------|-----------------------------------|
| -                | Regular trading                   |
| A                | Other auction (e.g. VWAP auction) |
| C                | Closing auction                   |
| O                | Opening auction                   |
| T                | Trading at closing price          |
| U                | Unscheduled auction               |

#### TRADE_TYPE - Enumeration

|   Enumeration ID | Enumeration Description              |
|------------------|--------------------------------------|
|               16 | Market on Close trade                |
|               26 | Midpoint trade                       |
|               30 | Regular trade                        |
|               31 | Daily VWAP trade                     |
|               44 | Exception trade (VWAP)               |
|               46 | Exception trade (TWAP)               |
|               47 | Block trade                          |
|               54 | Market on Close trade (INAV)         |
|                6 | Crossing trade (Unintentional cross) |
|                8 | Closing price trade                  |

