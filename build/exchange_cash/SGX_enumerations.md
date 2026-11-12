# Singapore Exchange (SGX) Enumerations

Trades, quotes and bars from the Singapore Exchange (SGX) securities market, with history from July 2014, covering the Mainboard and Catalist as well as ETFs, REITs and bonds. Covered stocks include constituents of the Straits Times Index (STI); index values are in ST_IDX.

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
|                3 | Odd lot book              |
|                5 | Buy-in                    |

#### MKT_PHASE - Enumeration

| Enumeration ID         | Enumeration Description                       |
|------------------------|-----------------------------------------------|
| ADJUST                 | Adjustment (re-opening auction)               |
| BI                     | Buy-in only                                   |
| BI_OPEN                | Buy-in open                                   |
| CIRB                   | Circuit breaker cooling-off period            |
| CIRH                   | Circuit breaker halt                          |
| CLOSE                  | Closed                                        |
| ```
| CLOSE_MKT              | Closed                                        |
| DL                     | Delisted                                      |
| H                      | Halted                                        |
| ICT                    | Instrument ceased trading                     |
| J                      | Adjustment (re-opening auction)               |
| MCE                    | Mandatory call event                          |
| MKT_ADJ                | Adjustment (re-opening auction)               |
| MKT_SUSP               | Market halt                                   |
| NON-CANCEL             | Non-cancel (auction uncrossing phase)         |
| NON-CANCEL_LAST        | Non-cancel (closing auction uncrossing phase) |
| OPEN                   | Continuous trading                            |
| PL                     | Pending listing                               |
| PRE-CLOSE              | Closing auction                               |
| PRE-OPEN               | Opening auction                               |
| PRE-OPEN1              | Opening auction                               |
| PRE-OPEN2              | Auction call                                  |
| REMOVE_ORDERS          | Halted, orderbook cleared                     |
| RIO                    | Halted, orderbook cleared                     |
| SOD                    | Start of day                                  |
| SUSP                   | Suspended                                     |
| TRADE_AT_CLOSE         | Trading at closing price                      |

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
| U                | Unscheduled auction       |

#### TRADE_TYPE - Enumeration

| Enumeration ID   | Enumeration Description           |
|------------------|-----------------------------------|
| 0                | Regular trade                     |
| 2                | Unintentional cross               |
| 512              | Regular trade (all or none)       |
| 514              | Unintentional cross (all or none) |
| RT               | Reported trade                    |

