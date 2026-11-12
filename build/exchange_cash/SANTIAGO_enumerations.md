# Santiago Stock Exchange Enumerations

Trades, quotes and bars from the Santiago Stock Exchange (Bolsa de Comercio de Santiago), Chile’s main exchange, with equities from November 2008 and indices from August 2021. Index data includes the IPSA, Chile’s main equity benchmark, which has been calculated by MSCI as the MSCI IPSA since September 2026 after being run by S&P Dow Jones Indices. The exchange is now part of the nuam regional exchange group with the Lima and Colombia exchanges.

The following fields have Enumerations:

* AUCTION_TYPE - Type of auction from which an indicative auction price / auction imbalance originates.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* STAT_INCLUSION_FLAG - “Y” - Trade counts towards price stats, “N” - Trade should be excluded from price stats
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

|   Enumeration ID | Enumeration Description       |
|------------------|-------------------------------|
|                0 | Lit order book                |
|                1 | Off-book [until 20210615]     |
|                6 | Auction book [until 20210615] |

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

#### STAT_INCLUSION_FLAG - Enumeration

| Enumeration ID   | Enumeration Description                 |
|------------------|-----------------------------------------|
| N                | Trade is excluded from price statistics |
| Y                | Trade is included in price statistics   |

#### TRADE_PERIOD - Enumeration

| Enumeration ID   | Enumeration Description                       |
|------------------|-----------------------------------------------|
| -                | Regular trading                               |
| A                | Other auction                                 |
| C                | Closing auction                               |
| I                | Intraday auction                              |
| L                | Outside hours (Late session) [until 20210615] |
| O                | Opening auction                               |
| U                | Unscheduled auction                           |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                                                                               |
|------------------|-------------------------------------------------------------------------------------------------------|
| ‘””’             | Regular trade                                                                                         |
| 1                | Opening [until 20210615]                                                                              |
| 10               | Local intermarket trade (order submitted to another exchange and executed on BCS) [until 20210615]    |
| 11               | External intermarket trade (order submitted to BCS and executed on another exchange) [until 20210615] |
| 2                | Continuous [until 20210615]                                                                           |
| 3                | Volatility auction [until 20210615]                                                                   |
| 4                | Closing [until 20210615]                                                                              |
| 5                | After hours [until 20210615]                                                                          |
| 6                | Open outcry auction [until 20210615]                                                                  |
| 7                | Electronic auction [until 20210615]                                                                   |
| 8                | Floor trade [until 20210615]                                                                          |
| 9                | Serialized auction [until 20210615]                                                                   |

