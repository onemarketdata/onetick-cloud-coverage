# Tokyo Stock Exchange (+ Fukuoka / Sapporo) Enumerations

Trades, quotes and bars from the Tokyo Stock Exchange (TSE), Japan’s main stock exchange and part of Japan Exchange Group, with history from October 2008, plus the separate regional Fukuoka and Sapporo exchanges. Since April 2022 TSE equities have been listed on the Prime, Standard and Growth markets, alongside the TOKYO PRO Market for professional investors. Main benchmarks are TOPIX, calculated by TSE, and the Nikkei 225.

The following fields have Enumerations:

* ASK_COND - Quote condition applicable to the best ask
* BID_COND - Quote condition applicable to the best bid
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_SESSION - Trading session from which a trade originates, e.g. “Day”, “Night”
* TRADE_TYPE - Type of trade

#### ASK_COND - Enumeration

|   Enumeration ID | Enumeration Description                                                                                                                   |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
|                0 | No bid                                                                                                                                    |
|                1 | Regular ask                                                                                                                               |
|                2 | Regular ask (buying up) [intermediate quote when an incoming order trades through multiple price points]                                  |
|                3 | Pre-open ask                                                                                                                              |
|                4 | Special ask [circuit breaker to prevent an excessive drop in price from one trade to the next - ask set to the lower limit]               |
|                5 | Sequential execution ask [circuit breaker caused by a large drop in price from a rapid string of executions - ask set to the lower limit] |

#### BID_COND - Enumeration

|   Enumeration ID | Enumeration Description                                                                                                                    |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
|                0 | No bid                                                                                                                                     |
|                1 | Regular bid                                                                                                                                |
|                2 | Regular bid (selling down) [intermediate quote when an incoming order trades through multiple price points]                                |
|                3 | Pre-open bid                                                                                                                               |
|                4 | Special bid [circuit breaker to prevent an excessive increase in price from one trade to the next - bid set to the upper limit]            |
|                5 | Sequential execution bid [circuit breaker caused by a large price increase from a rapid string of executions - bid set to the upper limit] |

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
| U                | Unscheduled auction       |

#### TRADE_SESSION - Enumeration

|   Enumeration ID | Enumeration Description      |
|------------------|------------------------------|
|                0 | Off-market trading (ToSTNet) |
|                1 | Morning session              |
|                2 | Afternoon session            |

#### TRADE_TYPE - Enumeration

|   Enumeration ID | Enumeration Description                           |
|------------------|---------------------------------------------------|
|                0 | Regular trade                                     |
|               10 | ToSTNeT single-issue transaction                  |
|               11 | ToSTNeT basket transaction                        |
|               12 | ToSTNeT previous day closing price transaction    |
|               13 | ToSTNeT previous day VWAP transaction             |
|               14 | ToSTNeT morning session closing price transaction |
|               15 | ToSTNeT morning session VWAP transaction          |
|               16 | ToSTNeT closing price transaction                 |
|               17 | ToSTNeT afternoon session VWAP transaction        |
|               18 | ToSTNeT daily VWAP transaction                    |

