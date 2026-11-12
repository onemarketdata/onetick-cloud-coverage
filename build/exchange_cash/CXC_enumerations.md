# Nasdaq CXC Enumerations

Trades, Quotes and Book depth from Nasdaq CXC (formerly Chi-X Canada), Nasdaq Canada’s main lit order book, with history from May 2017. It trades TSX- and TSX Venture-listed securities and is one of the largest alternative venues in Canada. Covered stocks include constituents of the S&P/TSX 60.   A consolidated tape for all Canadian equity markets is provided in the CA_COMP dataset.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* BYPASS - Identifies whether the trade resulted from a Bypass order
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* ODD_LOT - Indicates whether a trade was an odd lot
* ORDER_TYPE - Type of order.
* SPECIAL_TERMS - Indicates any non-standard settlement / execution terms associated with a trade
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade
* UPDATE_TYPE - Type of update

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description                          |
|------------------|--------------------------------------------------|
| ‘””’             | Undefined (e.g. off-book trades, auction trades) |
| B                | Buy                                              |
| S                | Sell                                             |

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |
|                3 | Odd lot book              |
|                4 | Special terms book        |

#### BYPASS - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Not a bypass trade        |
| Y                | Bypass trade              |

#### MKT_PHASE - Enumeration

| Enumeration ID   | Enumeration Description                  |
|------------------|------------------------------------------|
| C                | End of transmission                      |
| E                | End of system hours                      |
| H                | Halted                                   |
| M                | End of market hours                      |
| O                | Start of messages                        |
| Q                | Start of market hours                    |
| R                | Resume after market-wide circuit breaker |
| S                | Start of system hours                    |
| T                | Trading                                  |
| W                | Market-wide circuit breaker              |

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

#### ODD_LOT - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Board lot                 |
| Y                | Odd lot                   |

#### ORDER_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| L                | Limit order               |
| M                | Market order              |

#### SPECIAL_TERMS - Enumeration

| Enumeration ID   | Enumeration Description                |
|------------------|----------------------------------------|
| ‘””’             | No special terms (standard settlement) |
| CT               | Cash today                             |
| DD               | Delayed delivery                       |
| ND               | Next day                               |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description           |
|------------------|-----------------------------------|
| -                | Regular trading                   |
| C                | Closing auction (Market on close) |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                    |
|------------------|--------------------------------------------|
| ‘””’             | Regular trade                              |
| B                | Basis cross                                |
| C                | Contingent cross                           |
| D                | Derivative-related cross                   |
| H                | Hidden order execution                     |
| I                | Internal cross                             |
| N                | NAV cross                                  |
| L                | M-ELO (Midpoint Extended Life Order) trade |
| V                | VWAP cross                                 |
| X                | Intentional cross                          |

#### UPDATE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| A                | Add                       |
| D                | Delete                    |
| F                | Fill                      |
| M                | Modify                    |
| P                | Partial fill              |

