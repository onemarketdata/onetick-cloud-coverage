# BSE (Bombay Stock Exchange) Enumerations

Trades, quotes and bars from BSE (formerly the Bombay Stock Exchange), with equities history from September 2014 and futures and options from February 2026. Located on Dalal Street in Mumbai, BSE is one of India’s largest securities markets. Its benchmark is the Sensex, a free-float market-weighted index of 30 well-established Indian companies, and its derivatives segment includes index futures and options.

The following fields have Enumerations:

* AUCTION_TYPE - Type of auction from which an indicative auction price / auction imbalance originates.
* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* CALL_PUT_IND - “C” - Call option, “P” - Put option
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
|                3 | Odd lot book              |

#### CALL_PUT_IND - Enumeration

| Enumeration ID   | Enumeration Description   |
|------------------|---------------------------|
| C                | Call option               |
| P                | Put option                |

#### MKT_PHASE - Enumeration

| Enumeration ID   | Enumeration Description                   |
|------------------|-------------------------------------------|
| ‘””’             | No market phase                           |
| A                | Periodic call auction                     |
| CAF              | Closing auction freeze                    |
| CAM              | Closing auction end of matching           |
| CAO              | Closing auction start of order entry      |
| CS               | Closing session                           |
| CTE              | End of continuous trading                 |
| EMO              | Closing auction end of market order entry |
| CTN              | Continuous trading                        |
| EOD              | End of day session                        |
| MQ               | Member query                              |
| OM               | Order matching                            |
| PCS              | Post-close session                        |
| PO               | Pre-open                                  |
| SOD              | Start of day                              |
| SUSP             | Suspended                                 |

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
| I                | Intraday auction          |
| O                | Opening auction           |
| T                | Trading at closing price  |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description                                                                       |
|------------------|-----------------------------------------------------------------------------------------------|
| ‘””’             | Regular trade                                                                                 |
| BLK              | Block trade                                                                                   |
| BT               | Bunched trade [Aggregated trade where the individual executions are not sent by the exchange] |

