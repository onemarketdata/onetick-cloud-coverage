# TSX Venture Exchange Enumerations

Trades, quotes, bars and book depth from the TSX Venture Exchange, Canada’s market for early-stage and small-cap companies, with history from November 2017. It lists many junior mining and exploration companies and also covers the NEX board for companies that no longer meet TSXV listing requirements. Covered stocks include constituents of the S&P/TSX Venture Composite.   A consolidated tape for all Canadian equity markets is provided in the CA_COMP dataset.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* AUCTION_TYPE - Type of auction from which an indicative auction price / auction imbalance originates.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* BYPASS - Identifies whether the trade resulted from a Bypass order
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* ODD_LOT - Indicates whether a trade was an odd lot
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
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
|                3 | Odd lot book              |
|                4 | Special terms book        |

#### BYPASS - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Not a bypass trade        |
| Y                | Bypass trade              |

#### MKT_PHASE - Enumeration

| Enumeration ID   | Enumeration Description                   |
|------------------|-------------------------------------------|
| A                | CCP determination                         |
| AE               | Price movement delayed                    |
| AR               | Delayed open                              |
| AS               | Halted                                    |
| C                | Closed                                    |
| E                | Price movement extension                  |
| F                | Extended hours close                      |
| G                | NAVex order entry [until 20221230]        |
| H                | End of NAVex order entry [until 20221230] |
| I                | Inhibited                                 |
| IE               | Inhibited, volatility halt                |
| IR               | Inhibited, delayed open                   |
| IS               | Inhibited, halted                         |
| J                | NAVex closed [until 20221230]             |
| K                | NAVex AM execution [until 20221230]       |
| L                | Closing                                   |
| M                | MOC imbalance                             |
| N                | Extended hours CXLs                       |
| O                | Opening                                   |
| P                | Pre-open                                  |
| R                | Extended hours open                       |
| S                | Open                                      |
| T                | MOC freeze                                |
| X                | NAVex PM execution [until 20221230]       |
| Y                | NAVex closed [until 20221230]             |

#### ODD_LOT - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Board lot                 |
| Y                | Odd lot                   |

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

#### ORDER_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| L                | Limit order               |
| M                | Market order              |

#### SPECIAL_TERMS - Enumeration

| Enumeration ID   | Enumeration Description                |
|------------------|----------------------------------------|
| ‘””’             | No special terms (standard settlement) |
| C                | Cash                                   |
| CT               | Cash today                             |
| DC               | Derivative-related contingent trade    |
| DD               | Delayed delivery                       |
| NN               | Non-net                                |
| NR               | Non-resident                           |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| -                | Regular trading           |
| C                | Closing auction           |
| O                | Opening auction           |
| T                | Trading at closing price  |
| U                | Unscheduled auction       |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description               |
|------------------|---------------------------------------|
| ‘””’             | Regular trade                         |
| 6                | Dark conditional trade                |
| 7                | NAV cross                             |
| C                | Contingent cross                      |
| G                | VWAP cross                            |
| H                | Dark Contra Midpoint Only (CMO) trade |
| I                | Derivative-related cross              |
| J                | Regular (intentional) cross           |
| O                | Basis cross                           |
| S                | Special Trading Session cross         |
| X                | Internal cross                        |

#### UPDATE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| A                | Add                       |
| D                | Delete                    |
| F                | Fill                      |
| M                | Modify                    |
| P                | Partial fill              |

