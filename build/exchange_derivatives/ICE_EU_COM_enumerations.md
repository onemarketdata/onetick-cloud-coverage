# ICE Europe Commodities Enumerations

Futures, options and spreads with Trades, Quotes, bars and book depth from ICE Futures Europe’s commodity markets, with history from November 2009. It is home to Brent crude futures, the global oil benchmark, plus gasoil, UK natural gas (NBP), London cocoa, robusta coffee, white sugar and EU emissions futures.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* CALL_PUT_IND - “C” - Call option, “P” - Put option
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* ORDER_TYPE - Type of order.
* TRADE_TYPE - Type of trade

#### AGGRESSOR_SIDE - Enumeration

| Enumeration ID   | Enumeration Description                                          |
|------------------|------------------------------------------------------------------|
| ‘””’             | Undefined (e.g. auction trades, implied trades, off-book trades) |
| B                | Buy                                                              |
| S                | Sell                                                             |

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

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| 1                | Pre-open                  |
| 2                | Pre-close                 |
| C                | Closed                    |
| E                | Expired                   |
| O                | Open                      |

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
| I                | Implied order             |
| L                | Limit order               |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                                  |
|------------------|----------------------------------------------------------|
| 0                | Standard trade                                           |
| AA               | Asset Allocation                                         |
| AAL              | Asset allocation leg trade (System priced)               |
| ADJ              | Adjusted trade                                           |
| BAS              | Basis trade                                              |
| BLK              | Block trade                                              |
| BLKC             | Block crack leg trade (System priced)                    |
| BLKL             | Block leg trade (System priced)                          |
| BLKS             | Block composite strategy leg trade (System priced)       |
| BLT              | Bilateral block trade                                    |
| COMP             | Composite strategy leg trade (System priced)             |
| CRK              | Crack leg trade (System priced)                          |
| EFM              | Exchange of Futures for Related Market (EFM)             |
| EFP              | Exchange for Physical (EFP)                              |
| EFPC             | EFP/EFS Contra Trade [until July 2015]                   |
| EFS              | Exchange for Swap (EFS)                                  |
| EFSP             | EFS/EFP trade                                            |
| EOO              | Exchange of Options for Options (EOO)                    |
| GCR              | Guaranteed Cross                                         |
| IMO              | Implied spread trade at market open                      |
| IMP              | Implied trade (Standard trade against implied liquidity) |
| IPL              | Implied trade outside Interval Price Limits              |
| LEG              | Strategy leg trade (System priced)                       |
| RFC              | Request for Cross (RFC) trade                            |
| RFCL             | RFC Cross leg trade                                      |
| TAM              | Trade at Market                                          |

