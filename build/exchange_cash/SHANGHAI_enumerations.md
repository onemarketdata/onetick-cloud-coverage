# Shanghai Stock Exchange - Equities Enumerations

Trades, quotes, bars and book depth from the Shanghai Stock Exchange (SSE), with history from January 2015, covering the main board and STAR Market, A-shares and B-shares, and Shanghai-Hong Kong Stock Connect. Covered stocks include constituents of the SSE Composite, SSE 50 and CSI 300; index values are in SHANGHAI_IDX.

The following fields have Enumerations:

* AGGRESSOR_SIDE - Indicates whether a trade resulted from an incoming buy or sell order.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* TRADE_PERIOD - Market period during which a trade was executed.
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

#### MKT_PHASE - Enumeration

| Enumeration ID   | Enumeration Description                                       |
|------------------|---------------------------------------------------------------|
| 1                | Start of day                                                  |
| 10               | Period between end of auction and start of continuous trading |
| 2                | Auction                                                       |
| 3                | Continuous trading                                            |
| 4                | Break                                                         |
| 5                | End of trading                                                |
| 6                | Suspended                                                     |
| 8                | Circuit breaker                                               |
| 9                | Circuit breaker + close                                       |
| ADD              | Pre-listing                                                   |
| CCALL            | Closing auction                                               |
| CLOSE            | Closed                                                        |
| ENDTR            | End of trading day                                            |
| OCALL            | Opening auction                                               |
| START            | Resume                                                        |
| SUSP             | Suspended                                                     |
| TRADE            | Continuous trading                                            |

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

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| ‘””’             | Regular trade             |

