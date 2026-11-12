# Ho Chi Minh Stock Exchange Enumerations

Trades, quotes and bars from the Ho Chi Minh Stock Exchange (HOSE), Vietnam’s largest stock exchange, with history from August 2011. It lists just over 400 companies and trades stocks, closed-end fund certificates, ETFs, covered warrants and bonds. Index data is included, covering the VN-Index, which tracks all HOSE-listed stocks, and the VN30 of the 30 largest companies.

The following fields have Enumerations:

* BOOK_TYPE - Type of order book or trading mechanism through which a trade was executed.
* MKT_PHASE - Indicates the instrument’s current market phase, as specified by the trading venue
* OMD_STATUS - Indicates an instrument’s current trading status. Values are normalized across all DBs.
* TRADE_PERIOD - Market period during which a trade was executed.
* TRADE_TYPE - Type of trade

#### BOOK_TYPE - Enumeration

|   Enumeration ID | Enumeration Description   |
|------------------|---------------------------|
|                0 | Lit order book            |
|                1 | Off-book                  |
|                3 | Odd lot book              |
|                5 | Buy-in / Sell-out         |

#### MKT_PHASE - Enumeration

|   Enumeration ID | Enumeration Description                              |
|------------------|------------------------------------------------------|
|                1 | Opening auction call                                 |
|               10 | Circuit breaker notice                               |
|               11 | Circuit breaker notice clear                         |
|               12 | Circuit breaker suspension                           |
|               13 | Interface connection cut-off                         |
|               15 | Lunch break                                          |
|               16 | Open after lunch break                               |
|               17 | Board start                                          |
|               18 | Continuous trading                                   |
|               19 | Closing auction call                                 |
|                2 | Continuous trading                                   |
|               20 | Continuous trading resumed after market halt         |
|               21 | Continuous trading resumed after circuit breaker     |
|               22 | Closing periodic call auction                        |
|               23 | Periodic call auction open                           |
|               24 | Periodic call auction execution                      |
|               25 | Close of trading for restricted instruments          |
|               26 | Closing auction execution for restricted instruments |
|               27 | Trading halt released                                |
|               28 | Halted                                               |
|               29 | Continuous trading resumed after halt                |
|                3 | Trading board closed                                 |
|               30 | GTC/GTD orders reissued                              |
|                4 | Closing auction execution                            |
|                5 | Start of order entry                                 |
|                6 | Auction execution                                    |
|                7 | Market halt release                                  |
|                8 | Market halt                                          |
|                9 | Circuit breaker auction                              |

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
| U                | Unscheduled auction       |

#### TRADE_TYPE - Enumeration

|   Enumeration ID | Enumeration Description                |
|------------------|----------------------------------------|
|                0 | Regular trade                          |
|               10 | Negotiated trade (odd lot, post-close) |
|               11 | Negotiated trade (repo)                |
|               17 | Off-hours trade [until 20250429]       |
|                2 | Negotiated trade                       |
|                3 | Odd lot trade                          |
|                4 | Buy-in                                 |
|                5 | Sell-out                               |
|                7 | Negotiated trade (pre-open)            |
|                8 | Negotiated trade (post-close)          |
|                9 | Negotiated trade (odd lot)             |

